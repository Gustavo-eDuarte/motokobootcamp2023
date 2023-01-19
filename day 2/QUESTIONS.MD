1. Who controls the ledger canister? <br>
A - The NNS.<br>
<br>
2. What is the subnet of the canister with the id: mwrha-maaaa-aaaab-qabqq-cai? How many nodes are running this subnet?<br>
A - The subnet is pae4o-o6dxf-xki7q-ezclx-znyd6-fnk6w-vkv5z-5lfwh-xym2i-otrrw-fqe and there are 16 nodes running on it.<br>
<br>
3. I have a neuron with 1O ICPs locked with a dissolve delay of 4 years - my neuron has been locked for 2 years. What is my expected voting power?<br>
A - Voting Power = (ICP staked + maturity staked) x Dissolve Delay Bonus x Age Bonus. 10*1,5*1,125 = 16,875 of voting power.<br>
<br>
4. What is wrong with the following code?<br>
actor {
  let n : Nat = 50;
  let t : Text = "Hello";

  public func convert_to_text(m : Nat) : async Text {
    Nat.toText(m);
  };
 
}<br>
A - Need to import the following module import Nat "mo:base/Nat";<br>
<br>
5. What is wrong with the following code?<br>
actor {
  var languages : [var Text] = ["English", "German", "Chinese", "Japanese", "French"];

  public func show_languages(language : Text) : async [var Text] {
    return (languages);
  };
 
}<br>
A - Mutable data must always be kept private and can never be shared remotely. The variable "var text" should be in an immutable state.<br>
<br>
6. What is wrong with the following code?<br>
actor {
  var languages : [Text] = ["English", "German", "Chinese", "Japanese", "French"];

  public func add_language(new_language: Text) : async [Text] {
    languages := Array.append<Text>(languages, [new_language]);
    return (languages);
  };
 
}<br>
A - Need to import the following module import Array "mo:base/Array";