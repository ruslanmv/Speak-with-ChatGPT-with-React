```
const matrix_animated = (
<div style={{ position: 'relative', zIndex: 1, background: '#000000', minHeight: '100vh', display: 'flex', flexDirection: 'column', justifyContent: 'center', alignItems: 'center', fontFamily: 'Courier New, monospace' }}>    
<div className="matrix-background">
      {Array(100).fill(null).map((_, index) => (
        <span key={index} style={{ animationDuration: `${Math.random() * 5 + 3}s`, animationDelay: `${Math.random() * 3}s`, left: `${index * 20}px`, top: `${Math.random() * 100}vh` }}>1 0 1 0 1 0 1 0 1 0 1 0 1 0 1 0 1 0 1 0</span>
      ))}
    </div>
    <h1 style={{ fontSize: '48px', color: '#00FF00', marginBottom: '40px', fontFamily: '"Matrix Code NFI", monospace' }}>Speak with ChatGPT</h1>
    {!recording ? (
      <button onClick={startRecording} style={{ background: '#000000', color: '#00FF00', fontSize: '24px', padding: '10px 20px', borderRadius: '5px', border: '2px solid #00FF00', cursor: 'pointer', marginBottom: '20px', boxShadow: '0 3px 5px rgba(0,255,0,0.3)' }}>Start Recording</button>
    ) : (
      <button onClick={stopRecording} style={{ background: '#000000', color: '#00FF00', fontSize: '24px', padding: '10px 20px', borderRadius: '5px', border: '2px solid #00FF00', cursor: 'pointer', marginBottom: '20px', boxShadow: '0 3px 5px rgba(0,255,0,0.3)' }}>Stop Recording</button>
    )}
    <p style={{ fontSize: '24px', color: '#00FF00', maxWidth: '80%', lineHeight: '1.5', textAlign: 'left', background: '#000000', padding: '20px', borderRadius: '5px', boxShadow: '0 1px 3px rgba(0,255,0,0.2)' }}>User: {transcription}</p>
    {isLoading ? (
      <div style={{ fontSize: '24px', color: '#00FF00', maxWidth: '80%', lineHeight: '1.5', textAlign: 'left', background: '#000000', padding: '20px', borderRadius: '5px', boxShadow: '0 1px 3px rgba(0,255,0,0.2)' }}>
         <span style={{ fontSize: '20px', fontWeight: 'bold', color: '#00FF00', textShadow: '1px 1px 2px rgba(0,0,0,0.4)' }}>Processing...</span>
      </div>
    ) : (
      <p style={{ fontSize: '24px', color: '#00FF00', maxWidth: '80%', lineHeight: '1.5', textAlign: 'left', background: '#000000', padding: '20px', borderRadius: '5px', boxShadow: '0 1px 3px rgba(0,255,0,0.2)' }}>AI: {messageAI}</p>
    )}
  </div>
);

return (matrix_animated);

```