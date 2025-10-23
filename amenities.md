---
layout: default
title: Amenities
permalink: /amenities/
---

# Amenities

## Overview

The Amenities feature in Latch allows you to manage and showcase your property's facilities to your tenants. You can create bookable amenities that tenants can reserve through the Latch mobile app, ensuring fair access and preventing conflicts.

This guide will walk you through setting up a bookable cinema room, but the same principles apply to any bookable amenity such as meeting rooms, gyms, co-working spaces, or other shared facilities.

## What You Can Do With Amenities

- **Display facilities to tenants**: All amenities are visible to tenants in their mobile app
- **Enable tenant bookings**: Allow tenants to book amenities themselves
- **Enable staff bookings**: Allow your staff to make bookings on behalf of tenants or for events
- **Set opening hours**: Control when amenities are available for booking
- **Limit booking duration**: Set minimum and maximum booking lengths
- **Control capacity**: Set maximum participants for bookings
- **Private or public bookings**: Choose whether other tenants can see and join bookings
- **Add photos and descriptions**: Help tenants understand what each amenity offers

## Example Use Case: Cinema Room

This guide demonstrates setting up a cinema room for a 220-flat building with the following requirements:

- **Tenant bookable**: Residents can book through the mobile app
- **Private bookings**: Only one booking at a time (no overlapping reservations)
- **Time restrictions**: Available only between 6 PM and 11 PM
- **Booking duration limits**: Minimum 1 hour, maximum 3 hours
- **Capacity**: Up to 20 people
- **Free to use**: No charges for tenants

---

## Step-by-Step: Creating a Bookable Cinema Room

### Step 1: Access the Amenities Section

1. Log in to your Latch portal at your portal URL
2. From the left navigation menu, click on **Amenities**

![Amenities Menu](/assets/images/03-amenities-list.png)

You'll see a list of all your current amenities with their descriptions and future booking counts.

### Step 2: Start Creating a New Amenity

1. Click the **Create Amenity** button in the top right corner
2. You'll see an introduction dialog explaining the amenities feature

![Create Amenity Dialog](/assets/images/04-create-amenity-intro.png)

The dialog provides examples of different amenity types:
- Non-bookable amenities (like a lounge anyone can use)
- Tenant-bookable amenities (like a cinema room)
- Staff-bookable amenities (like a gym studio for classes)
- Paid bookable amenities (like a private meeting room)

3. Click **Get Started** to proceed

### Step 3: Enter Amenity Details

Now you'll fill in the basic information about your amenity. All fields marked with an asterisk (*) are required.

![Amenity Details Form](/assets/images/05-amenity-details-form.png)

Complete the following fields:

#### Required Fields:

**Amenity Name***
- Enter a clear, descriptive name
- Example: `Premium Cinema Room` or `Community Cinema`

**Type***
- Click the dropdown to select from available amenity types
- For a cinema, select **Movie-room**
- If you need a type that isn't listed, click the "Request more types here" link to email support

**Description***
- Provide a detailed description that will be visible to tenants
- Include key features, equipment, and what makes the space special
- Example:
  ```
  Enjoy a premium viewing experience in our state-of-the-art cinema room.
  Features include a large screen, surround sound system, and comfortable
  seating for up to 20 people. Perfect for movie nights with friends and family.
  ```

#### Optional Fields:

**Location**
- Specify where tenants can find the amenity
- Example: `Ground Floor, East Wing`

**Rules**
- Add any usage rules or guidelines
- Example:
  ```
  Please keep noise levels down. No food or drinks except for sealed containers.
  Clean up after use. Maximum 20 people at a time.
  ```

**Opening Time*** and **Closing Time***
- Set the hours when the amenity is available
- For a cinema room available from 6 PM to 11 PM, enter:
  - Opening Time: `18:00`
  - Closing Time: `23:00`
- Use 24-hour format (e.g., 18:00 for 6 PM, 23:00 for 11 PM)

![Filled Amenity Details](/assets/images/06-amenity-details-filled.png)

4. Once all required fields are completed, click **Next**

### Step 4: Configure Booking Settings

The second step is where you control who can book the amenity and set booking restrictions.

![Booking Configuration](/assets/images/07-booking-config-initial.png)

#### Bookable By

Select who can make bookings:
- **Not bookable**: Amenity is visible but cannot be booked
- **Staff**: Only staff members can make bookings (useful for classes or events)
- **Tenants**: Tenants can book the amenity themselves via the mobile app

For our cinema room example, select **Tenants**.

#### Tenant Booking Configuration

When you select "Tenants" as bookable by, additional options appear:

![Tenant Booking Options](/assets/images/08-tenant-booking-options.png)

**Tenant Booking Type**
- **Private only**: Only one booking at a time; other tenants cannot see or join
- **Public**: Other tenants can discover and join the booking

For a cinema room where you want to prevent multiple simultaneous bookings, select **Private only**.

**Minimum Booking Length (minutes)**
- Set the shortest time a tenant can book
- For a cinema room, `60` minutes (1 hour) ensures meaningful use

**Maximum Booking Length (minutes)**
- Set the longest time a tenant can book
- For a cinema room, `180` minutes (3 hours) allows for a full movie viewing
- This prevents one tenant from monopolizing the space

**Booking Step (minutes)**
- Set the time interval for booking slots
- For example, `30` minutes allows bookings to start at 6:00 PM, 6:30 PM, 7:00 PM, etc.
- A `60` minute step would only allow bookings on the hour (6:00 PM, 7:00 PM, etc.)

**Maximum Participants**
- Set the capacity for the amenity
- For a cinema room with 20 seats, enter `20`
- This field is required for private tenant bookings or public bookings

![Filled Booking Configuration](/assets/images/09-booking-config-filled.png)

#### Example Configuration Summary

For our cinema room:
- **Bookable by**: Tenants
- **Tenant Booking**: Private only
- **Minimum Booking Length**: 60 minutes
- **Maximum Booking Length**: 180 minutes
- **Booking Step**: 30 minutes
- **Maximum Participants**: 20 people

5. Once configured, click **Complete** to create the amenity

The system will create your amenity and return you to the amenities list.

### Step 5: Review Your New Amenity

After creation, you'll see your new amenity in the list:

![Amenities List with New Cinema](/assets/images/10-amenities-list-with-new.png)

Click on the amenity name to view its details page.

### Step 6: Amenity Details and Management

The amenity details page has several sections:

![Amenity Details - Bookings Tab](/assets/images/11-amenity-details-bookings.png)

#### Details Section

Shows all the information you entered:
- **Type**: The amenity category with its icon
- **Location**: Where tenants can find it
- **Rules**: Usage guidelines
- **Opening Times**: When the amenity is available

You can click **Edit** to modify any of these details or **Delete** to remove the amenity.

#### Photos Section

Add photos of your amenity to help tenants visualize the space:
1. Click the **+** button to upload photos
2. Photos will be visible to tenants in the mobile app

#### Bookings Tab

The **Bookings** tab shows a calendar view of all current and future bookings:
- View bookings by week
- See available time slots (in this example, 6 PM to 11 PM each day)
- Click **Add Booking** to create bookings on behalf of tenants (staff only)
- Navigate between weeks using the arrow buttons

#### Configuration Tab

![Amenity Configuration Tab](/assets/images/12-amenity-configuration.png)

The **Configuration** tab displays all the booking settings you configured:
- **Bookable By**: Staff, Tenants (or just one)
- **Tenant Booking Type**: Private only or Public
- **Minimum Booking Length**: 60 minutes
- **Maximum Booking Length**: 180 minutes
- **Booking Step**: 30 minutes
- **Maximum Participants**: 20 people

To change these settings, click **Edit** in the Details section and navigate through the amenity creation flow again.

---

## How Tenants Book the Cinema Room

Once you've created the amenity, tenants can:

1. **Open the Latch mobile app** on their phone
2. **Navigate to the Amenities section**
3. **Select the Premium Cinema Room** from the list
4. **View details**: See photos, description, rules, and location
5. **Choose a date and time**: Select an available slot within the 6 PM - 11 PM window
6. **Select duration**: Choose between 1 and 3 hours (in 30-minute increments)
7. **Confirm the booking**: Submit the reservation
8. **Receive confirmation**: Get a booking confirmation in the app

Because the bookings are set to "Private only," once a tenant books a time slot, that time becomes unavailable to other tenants, preventing double bookings.

---

## Managing Bookings

As a staff member, you can:

### View All Bookings
- Go to the amenity details page
- Click the **Bookings** tab
- Use the calendar view to see all reservations
- Navigate between weeks using the arrow buttons

### Create Bookings on Behalf of Tenants
1. Click **Add Booking**
2. Select the tenant
3. Choose date, time, and duration
4. Confirm the booking

### Cancel or Modify Bookings
- Click on an existing booking in the calendar
- View booking details
- Cancel or modify as needed

---

## Tips and Best Practices

### Setting Opening Hours
- Consider your building's quiet hours and community guidelines
- For a cinema, evening hours (6 PM - 11 PM) are typical
- You can create multiple amenities for the same space with different rules (e.g., "Cinema - Daytime" and "Cinema - Evening")

### Booking Duration Limits
- **Minimum length**: Should be long enough for meaningful use (at least 1 hour for a cinema)
- **Maximum length**: Prevents monopolization while allowing sufficient time (2-3 hours for a movie)
- Balance fairness with practical usage patterns

### Private vs. Public Bookings
- **Private**: Best for exclusive use (cinema rooms, meeting rooms)
- **Public**: Better for classes or events where multiple tenants can participate

### Booking Steps
- **30-minute steps**: More flexibility, more booking slots
- **60-minute steps**: Simpler scheduling, fewer slots
- Choose based on typical usage patterns

### Capacity Management
- Set realistic maximum participants based on:
  - Physical space limitations
  - Seating capacity
  - Fire safety regulations
  - Comfort and experience quality

### Adding Photos
- Upload clear, well-lit photos of the amenity
- Show different angles and key features
- Update photos periodically to reflect improvements
- Photos significantly increase booking rates

### Rules and Guidelines
- Be clear and specific about usage rules
- Include cleanup expectations
- Mention any prohibited items or activities
- Specify consequences for rule violations
- Keep rules concise and easy to understand

---

## Troubleshooting

### Tenants Can't See the Amenity
- Ensure the amenity is saved and published
- Check that opening hours are set correctly
- Verify tenant app is up to date

### Booking Times Don't Appear
- Confirm opening and closing times are in 24-hour format
- Ensure opening time is before closing time
- Check that the booking step divides evenly into available hours

### Overlapping Bookings Occurring
- Verify "Private only" is selected for tenant booking type
- Check that minimum booking length doesn't allow gaps
- Review booking step settings

### Tenants Can't Book Desired Duration
- Review minimum and maximum booking length settings
- Ensure requested duration fits within opening hours
- Check that duration is a multiple of the booking step

---

## Frequently Asked Questions

**Q: Can I charge tenants to use amenities?**
A: Currently, the tenant booking flow does not include payment processing. However, staff bookings can include optional fees. Contact support for custom billing arrangements.

**Q: Can I create recurring bookings?**
A: Currently, each booking must be created individually. Contact support if you need recurring booking functionality.

**Q: Can I see booking history?**
A: Yes, in the Bookings tab, you can view past bookings by navigating to previous weeks using the arrow buttons.

**Q: Can I limit how many bookings a tenant can make?**
A: This feature is not currently available in the interface. Contact support if you need booking frequency limits.

**Q: What happens if a tenant doesn't show up?**
A: The booking remains in place and blocks that time slot. Consider implementing a cancellation policy in your rules section.

**Q: Can I send notifications about amenity bookings?**
A: Tenants receive automatic notifications when they create bookings. Staff notifications can be configured through your organization settings.

**Q: Can tenants book amenities for guests?**
A: The current system allows the booking tenant to bring guests up to the maximum participant limit. Guest details are not captured in the booking.

**Q: How far in advance can tenants book?**
A: This is configurable in your organization settings. Contact support to adjust the advance booking window.

---

## Summary

The Amenities feature is a powerful tool for managing shared spaces in your property:

1. **Create** amenities with detailed descriptions and photos
2. **Configure** booking rules to match your needs
3. **Set** opening hours and duration limits
4. **Choose** private or public booking types
5. **Manage** bookings through the calendar view
6. **Monitor** usage and adjust settings as needed

By following this guide, you've learned how to set up a fully functional bookable cinema room that tenants can reserve through the mobile app, with all the controls you need to ensure fair access and prevent conflicts.
