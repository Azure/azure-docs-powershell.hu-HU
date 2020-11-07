---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: 43eda2eb27003a079dae0442d7ab8e9f636cbef4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837454"
---
# <span data-ttu-id="5fb35-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="5fb35-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="5fb35-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5fb35-102">SYNOPSIS</span></span>
<span data-ttu-id="5fb35-103">Új akciócsoport-vevőkészülék létrehozása.</span><span class="sxs-lookup"><span data-stu-id="5fb35-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="5fb35-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5fb35-104">SYNTAX</span></span>

### <span data-ttu-id="5fb35-105">NewEmailReceiver (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5fb35-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fb35-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="5fb35-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fb35-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="5fb35-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fb35-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="5fb35-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fb35-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="5fb35-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fb35-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="5fb35-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fb35-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="5fb35-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fb35-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="5fb35-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fb35-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="5fb35-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fb35-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="5fb35-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fb35-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="5fb35-115">DESCRIPTION</span></span>
<span data-ttu-id="5fb35-116">A **New-AzActionGroupReceiver** parancsmag új műveleti csoportba foglalt vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="5fb35-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="5fb35-117">Példák</span><span class="sxs-lookup"><span data-stu-id="5fb35-117">EXAMPLES</span></span>

### <span data-ttu-id="5fb35-118">Példa 1: új e-mail-vevőkészülék létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="5fb35-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="5fb35-119">A parancs új e-mail-vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="5fb35-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="5fb35-120">2. példa: új SMS-vevőkészülék létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="5fb35-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="5fb35-121">A parancs új SMS-vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="5fb35-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="5fb35-122">3. példa: új webhook-vevőkészülék létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="5fb35-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="5fb35-123">A parancs új webhook-vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="5fb35-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="5fb35-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5fb35-124">PARAMETERS</span></span>

### <span data-ttu-id="5fb35-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="5fb35-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="5fb35-126">ArmRoleReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="5fb35-126">Create a ArmRoleReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewArmRoleReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="5fb35-127">-AutomationAccountId</span></span>
<span data-ttu-id="5fb35-128">a AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="5fb35-128">the AutomationAccountId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="5fb35-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="5fb35-130">AutomationRunbookReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="5fb35-130">Create a AutomationRunbookReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="5fb35-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="5fb35-132">az URI, ahová a webakasztókat el kell küldeni</span><span class="sxs-lookup"><span data-stu-id="5fb35-132">the URI where webhooks should be sent</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="5fb35-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="5fb35-134">a AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="5fb35-134">the AzureAppPushEmailAddress</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureAppPushReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="5fb35-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="5fb35-136">AzureAppPushReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="5fb35-136">Create a AzureAppPushReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAzureAppPushReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="5fb35-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="5fb35-138">ArmRoleReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="5fb35-138">Create a ArmRoleReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="5fb35-139">-CallbackUrl</span></span>
<span data-ttu-id="5fb35-140">a CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="5fb35-140">the CallbackUrl</span></span>

```yaml
Type: System.String
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="5fb35-141">-ConnectionId</span></span>
<span data-ttu-id="5fb35-142">a vevőkészülék ITSM-kapcsolat azonosítója</span><span class="sxs-lookup"><span data-stu-id="5fb35-142">the itsm connection id of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="5fb35-143">-CountryCode</span></span>
<span data-ttu-id="5fb35-144">Az SMS-vevőkészülék országkódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fb35-144">Specifies the country code for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fb35-145">-DefaultProfile</span></span>
<span data-ttu-id="5fb35-146">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5fb35-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="5fb35-147">-EmailAddress</span></span>
<span data-ttu-id="5fb35-148">Az E-mail címzett címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fb35-148">Specifies the address for the Email receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewEmailReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="5fb35-149">-EmailReceiver</span></span>
<span data-ttu-id="5fb35-150">E-mail-címzett létrehozásának megadása</span><span class="sxs-lookup"><span data-stu-id="5fb35-150">Specifies to create an Email receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewEmailReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="5fb35-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="5fb35-152">a Function app resourceId</span><span class="sxs-lookup"><span data-stu-id="5fb35-152">the function app resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-153">-Függvénynév</span><span class="sxs-lookup"><span data-stu-id="5fb35-153">-FunctionName</span></span>
<span data-ttu-id="5fb35-154">a függvénynév</span><span class="sxs-lookup"><span data-stu-id="5fb35-154">the functionName</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="5fb35-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="5fb35-156">a httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="5fb35-156">the httpTriggerUrl</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="5fb35-157">-IdentifierUri</span></span>
<span data-ttu-id="5fb35-158">az aad-hitelesítés azonosítójának URI azonosítója</span><span class="sxs-lookup"><span data-stu-id="5fb35-158">the Identifier uri for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="5fb35-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="5fb35-160">annak jelzése, hogy a példány globális runbook-e</span><span class="sxs-lookup"><span data-stu-id="5fb35-160">indicating whether this instance is global runbook</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="5fb35-161">-ItsmReceiver</span></span>
<span data-ttu-id="5fb35-162">ItsmReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="5fb35-162">Create a ItsmReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewItsmReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="5fb35-163">-LogicAppReceiver</span></span>
<span data-ttu-id="5fb35-164">LogicAppReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="5fb35-164">Create a LogicAppReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-165">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5fb35-165">-Name</span></span>
<span data-ttu-id="5fb35-166">A címzett nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fb35-166">Specifies the name for the receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5fb35-167">-ObjectId</span></span>
<span data-ttu-id="5fb35-168">a aad Auth webhook app Object ID</span><span class="sxs-lookup"><span data-stu-id="5fb35-168">the webhook app object Id for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-169">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="5fb35-169">-PhoneNumber</span></span>
<span data-ttu-id="5fb35-170">Az SMS-vevőkészülék telefonszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fb35-170">Specifies the phone number for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-171">-Region (régió)</span><span class="sxs-lookup"><span data-stu-id="5fb35-171">-Region</span></span>
<span data-ttu-id="5fb35-172">a vevőkészülék ITSM területe</span><span class="sxs-lookup"><span data-stu-id="5fb35-172">the itsm Region of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fb35-173">-ResourceId</span></span>
<span data-ttu-id="5fb35-174">a ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fb35-174">the ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="5fb35-175">-RoleId</span></span>
<span data-ttu-id="5fb35-176">A vevőkészülék kar szerepkör-azonosítója</span><span class="sxs-lookup"><span data-stu-id="5fb35-176">The arm role id of the receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewArmRoleReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="5fb35-177">-RunbookName</span></span>
<span data-ttu-id="5fb35-178">a RunbookName</span><span class="sxs-lookup"><span data-stu-id="5fb35-178">the RunbookName</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="5fb35-179">-ServiceUri</span></span>
<span data-ttu-id="5fb35-180">A webhook-vevőkészülék URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fb35-180">Specifies the URI for the webhook receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="5fb35-181">-SmsReceiver</span></span>
<span data-ttu-id="5fb35-182">Az SMS-vevőkészülék létrehozásának megadása</span><span class="sxs-lookup"><span data-stu-id="5fb35-182">Specifies to create a SMS receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-183">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="5fb35-183">-TenantId</span></span>
<span data-ttu-id="5fb35-184">a aad-hitelesítés bérlői azonosítója</span><span class="sxs-lookup"><span data-stu-id="5fb35-184">the tenant id for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="5fb35-185">-TicketConfiguration</span></span>
<span data-ttu-id="5fb35-186">a vevőkészülék ITSM TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="5fb35-186">the itsm TicketConfiguration of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="5fb35-187">-UseAadAuth</span></span>
<span data-ttu-id="5fb35-188">az Add Authentication bővítmény használatára szolgáló jelölő</span><span class="sxs-lookup"><span data-stu-id="5fb35-188">the flag to use add auth</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="5fb35-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="5fb35-190">A megjelölés a gyakori riasztási sémát használja-e.</span><span class="sxs-lookup"><span data-stu-id="5fb35-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="5fb35-191">Ezt az értéket az neglectedfor SMS, Azure app push, ITSM és Voice recievers fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="5fb35-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="5fb35-192">-VoiceCountryCode</span></span>
<span data-ttu-id="5fb35-193">A hangvevőkészülék országkódot</span><span class="sxs-lookup"><span data-stu-id="5fb35-193">The country code of the voice receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewVoiceReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="5fb35-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="5fb35-195">A hangvevőkészülék telefonszáma</span><span class="sxs-lookup"><span data-stu-id="5fb35-195">The phone number of the voice receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewVoiceReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="5fb35-196">-VoiceReceiver</span></span>
<span data-ttu-id="5fb35-197">Hangvevőkészülék létrehozása</span><span class="sxs-lookup"><span data-stu-id="5fb35-197">Create a voice receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewVoiceReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="5fb35-198">-WebhookReceiver</span></span>
<span data-ttu-id="5fb35-199">A webhook-vevőkészülék létrehozásának meghatározása</span><span class="sxs-lookup"><span data-stu-id="5fb35-199">Specifies to create a webhook receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="5fb35-200">-WebhookResourceId</span></span>
<span data-ttu-id="5fb35-201">a WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="5fb35-201">the WebhookResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="5fb35-202">-WorkspaceId</span></span>
<span data-ttu-id="5fb35-203">a vevőkészülék ITSM munkaterület-azonosítója</span><span class="sxs-lookup"><span data-stu-id="5fb35-203">the itsm workspace id of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb35-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fb35-204">CommonParameters</span></span>
<span data-ttu-id="5fb35-205">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5fb35-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fb35-206">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5fb35-206">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fb35-207">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fb35-207">INPUTS</span></span>

### <span data-ttu-id="5fb35-208">System. String</span><span class="sxs-lookup"><span data-stu-id="5fb35-208">System.String</span></span>

### <span data-ttu-id="5fb35-209">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5fb35-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5fb35-210">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fb35-210">OUTPUTS</span></span>

### <span data-ttu-id="5fb35-211">Microsoft. Azure. commands. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="5fb35-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="5fb35-212">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5fb35-212">NOTES</span></span>

## <span data-ttu-id="5fb35-213">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5fb35-213">RELATED LINKS</span></span>

<span data-ttu-id="5fb35-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="5fb35-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
