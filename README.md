if (event.getMessage().getContentRaw().equals("!bday")) { // Birthday present command.
            String ghostId = "4533452126647746576";  // Ghost's ID.
            String ID = event.getMessage().getAuthor().getId();  // Message author's ID.
            Role Owner = event.getGuild().getRoleById("556943820118556688"); // Owner role.
            if (ID.equals(ghostId)) { // If the message author is Ghost
                if (System.currentTimeMillis() >= 1581357600000L) { // and the day is currently Ghost's birthday,
                    event.getChannel().sendMessage("Happy birthday, <@4533452126647746576>!" +
                    " Here's something my creator made for you. If you'd like to see the source," +
                    " here's the Github. I wish you a good one!" +
                    " :confetti_ball: :partying_face:").queue();
                    event.getChannel().sendMessage("").queue(); // wish happy birthday,
                    Owner.getManager().setName("CoOwner").complete(); // Change "Owner" to "coOwner,"
                    event.getGuild().addRoleToMember(ghostId, Owner).queue(); // and add the role to Ghost.
                }
            }
        }
