## import { useState } from 'react';
import { Button } from '@/components/ui/button';
import { Input } from '@/components/ui/input';
import { Textarea } from '@/components/ui/textarea';

export default function ClassDiscussionApp() {
  const [user, setUser] = useState(null);
  const [name, setName] = useState('');
  const [email, setEmail] = useState('');
  const [isLoggedIn, setIsLoggedIn] = useState(false);
  const [assignment, setAssignment] = useState('');
  const [discussion, setDiscussion] = useState('');
  const [messages, setMessages] = useState([]);

  const handleRegister = () => {
    if (!name || !email) return alert("Jaza jina na email");
    const newUser = { name, email };
    setUser(newUser);
    setIsLoggedIn(true);
  };

  const handleSubmitAssignment = () => {
    if (!assignment) return alert("Andika majibu yako");
    alert("Assignment imetumwa. Asante " + user.name);
    setAssignment('');
  };

  const handlePostDiscussion = () => {
    if (!discussion) return;
    setMessages([...messages, { user: user.name, text: discussion }]);
    setDiscussion('');
  };

  return (
    <div className="p-4 max-w-2xl mx-auto">
      <h1 className="text-xl font-bold text-center mb-4">CLASS DISCUSSION BAIT-2024</h1>

      {!isLoggedIn ? (
        <div className="space-y-2">
          <Input placeholder="Jina" value={name} onChange={e => setName(e.target.value)} />
          <Input type="email" placeholder="Email" value={email} onChange={e => setEmail(e.target.value)} />
          <Button onClick={handleRegister}>Jiunge</Button>
        </div>
      ) : (
        <div className="space-y-4">
          <div className="flex justify-between items-center">
            <p>Karibu, <strong>{user.name}</strong></p>
            <Button variant="outline" onClick={() => { setIsLoggedIn(false); setUser(null); }}>Logout</Button>
          </div>

          <div>
            <h2 className="font-semibold mb-2">Tuma Majibu ya Assignment</h2>
            <Textarea value={assignment} onChange={e => setAssignment(e.target.value)} placeholder="Andika hapa..." />
            <Button className="mt-2" onClick={handleSubmitAssignment}>Tuma</Button>
          </div>

          <div>
            <h2 className="font-semibold mb-2">Mjadala wa Darasa</h2>
            <Textarea value={discussion} onChange={e => setDiscussion(e.target.value)} placeholder="Changia mawazo yako..." />
            <Button className="mt-2" onClick={handlePostDiscussion}>Tuma Maoni</Button>
            <div className="mt-4 space-y-2">
              {messages.map((msg, idx) => (
                <div key={idx} className="bg-gray-100 p-2 rounded">
                  <strong>{msg.user}</strong>: {msg.text}
                </div>
              ))}
            </div>
          </div>
        </div>
      )}
    </div>
  );
}

<!--
**bryton123/bryton123** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.
import { useState } from 'react';
import { Button } from '@/components/ui/button';
import { Input } from '@/components/ui/input';
import { Textarea } from '@/components/ui/textarea';

export default function ClassDiscussionApp() {
  const [user, setUser] = useState(null);
  const [name, setName] = useState('');
  const [email, setEmail] = useState('');
  const [isLoggedIn, setIsLoggedIn] = useState(false);
  const [assignment, setAssignment] = useState('');
  const [discussion, setDiscussion] = useState('');
  const [messages, setMessages] = useState([]);

  const handleRegister = () => {
    if (!name || !email) return alert("Jaza jina na email");
    const newUser = { name, email };
    setUser(newUser);
    setIsLoggedIn(true);
  };

  const handleSubmitAssignment = () => {
    if (!assignment) return alert("Andika majibu yako");
    alert("Assignment imetumwa. Asante " + user.name);
    setAssignment('');
  };

  const handlePostDiscussion = () => {
    if (!discussion) return;
    setMessages([...messages, { user: user.name, text: discussion }]);
    setDiscussion('');
  };

  return (
    <div className="p-4 max-w-2xl mx-auto">
      <h1 className="text-xl font-bold text-center mb-4">CLASS DISCUSSION BAIT-2024</h1>

      {!isLoggedIn ? (
        <div className="space-y-2">
          <Input placeholder="Jina" value={name} onChange={e => setName(e.target.value)} />
          <Input type="email" placeholder="Email" value={email} onChange={e => setEmail(e.target.value)} />
          <Button onClick={handleRegister}>Jiunge</Button>
        </div>
      ) : (
        <div className="space-y-4">
          <div className="flex justify-between items-center">
            <p>Karibu, <strong>{user.name}</strong></p>
            <Button variant="outline" onClick={() => { setIsLoggedIn(false); setUser(null); }}>Logout</Button>
          </div>

          <div>
            <h2 className="font-semibold mb-2">Tuma Majibu ya Assignment</h2>
            <Textarea value={assignment} onChange={e => setAssignment(e.target.value)} placeholder="Andika hapa..." />
            <Button className="mt-2" onClick={handleSubmitAssignment}>Tuma</Button>
          </div>

          <div>
            <h2 className="font-semibold mb-2">Mjadala wa Darasa</h2>
            <Textarea value={discussion} onChange={e => setDiscussion(e.target.value)} placeholder="Changia mawazo yako..." />
            <Button className="mt-2" onClick={handlePostDiscussion}>Tuma Maoni</Button>
            <div className="mt-4 space-y-2">
              {messages.map((msg, idx) => (
                <div key={idx} className="bg-gray-100 p-2 rounded">
                  <strong>{msg.user}</strong>: {msg.text}
                </div>
              ))}
            </div>
          </div>
        </div>
      )}
    </div>
  );
}
Here are some ideas to get you started:

