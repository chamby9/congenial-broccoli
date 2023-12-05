import React, { useState, useEffect } from 'react';
import NfcManager from 'react-nfc';

const App = () => {
  const [nfcId, setNfcId] = useState('');

  useEffect(() => {
    const handleNfcTagDetected = (tag) => {
      setNfcId(tag.identifier);
    };

    NfcManager.start({
      onTagDetected: handleNfcTagDetected,
    });

    return () => {
      NfcManager.stop({
        onTagDetected: handleNfcTagDetected,
      });
    };
  }, []);

  return (
    <div>
      <h1>Hello World!</h1>
      <p>NFC ID: {nfcId}</p>
    </div>
  );
};

export default App;
