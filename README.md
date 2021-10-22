import React, { Component } from 'react';
import { EditorState } from 'draft-js';
import { Editor } from 'react-draft-wysiwyg';

class MyEditor extends Component {
  constructor(props) {
    super(props);
    this.state = {
      editorState: EditorState.createEmpty()
    };
  }

  onEditorStateChange = editorState => {
    this.setState({
      editorState
    });
  };

  render() {
    const { editorState } = this.state;

    return (
      <div>
        <Editor
          editorState={editorState}
          wrapperClassName="rich-editor demo-wrapper"
          editorClassName="demo-editor"
          onEditorStateChange={this.onEditorStateChange}
          placeholder="The message goes here..."
        />
      </div>
    );
  }
}

export { MyEditor };
view rawmyEditor-1.js hosted with ❤ by GitHub
In our App.js file, react already gives us some default code but we shall replace it with the code below. Note that we also import the react-draft-wysiwyg.css from node_modules so that we get all the styles for our editor.
import React from 'react';
import { MyEditor } from './components/myEditor';
import './App.css'
import '../node_modules/react-draft-wysiwyg/dist/react-draft-wysiwyg.css';

function App() {
  return (
    <div className="app">
      <MyEditor />
    </div>
  );
}

export default App;
