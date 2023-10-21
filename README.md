# Module-task
import React, { Component } from 'react';
import { View, Text, TouchableOpacity, StyleSheet } from 'react-native';

class App extends Component {
  constructor(props) {
    super(props);
    this.state = {
      displayText: ''
    };
  }

  handleButtonPress = () => {
    const name = 'Your Name';
    const universityID = 'Your University ID';
    this.setState({ displayText: 'omar alebbini\n137077' });
  };

  render() {
    return (
      <View style={styles.container}>
        <TouchableOpacity style={styles.button} onPress={this.handleButtonPress}>
          <Text style={styles.buttonText}>click on</Text>
        </TouchableOpacity>
        <Text style={styles.displayText}>{this.state.displayText}</Text>
      </View>
    );
  }
}

const styles = StyleSheet.create({
  container: {
    backgroundColor:'white',
    flex: 1,
    justifyContent: 'space-evenly',
    alignItems: 'center',
  },
  button: {
    backgroundColor: 'blue',
    padding: 10,
    borderRadius: 8,
    marginBottom:20,
  },
  displayText: {
    fontSize: 30,
    padding:10,
    borderRadius:7,
    backgroundColor:'blue',
    color:'white',
    textAlign: 'center',
  },
  buttonText: {
    color: 'black',
    fontSize: 18,
  },
  
});

export default App;
