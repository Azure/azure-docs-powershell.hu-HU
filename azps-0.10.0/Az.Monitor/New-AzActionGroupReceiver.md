---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: e795f54fbcd31a8035e892a545b4afa1c2283366
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842010"
---
# <span data-ttu-id="0c00f-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="0c00f-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="0c00f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0c00f-102">SYNOPSIS</span></span>
<span data-ttu-id="0c00f-103">Új akciócsoport-vevőkészülék létrehozása.</span><span class="sxs-lookup"><span data-stu-id="0c00f-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="0c00f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0c00f-104">SYNTAX</span></span>

### <span data-ttu-id="0c00f-105">NewEmailReceiver (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0c00f-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c00f-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="0c00f-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c00f-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="0c00f-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c00f-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="0c00f-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c00f-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="0c00f-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c00f-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="0c00f-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c00f-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="0c00f-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c00f-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="0c00f-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c00f-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="0c00f-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c00f-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="0c00f-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c00f-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="0c00f-115">DESCRIPTION</span></span>
<span data-ttu-id="0c00f-116">A **New-AzActionGroupReceiver** parancsmag új műveleti csoportba foglalt vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="0c00f-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="0c00f-117">Példák</span><span class="sxs-lookup"><span data-stu-id="0c00f-117">EXAMPLES</span></span>

### <span data-ttu-id="0c00f-118">Példa 1: új e-mail-vevőkészülék létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="0c00f-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="0c00f-119">A parancs új e-mail-vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="0c00f-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="0c00f-120">2. példa: új SMS-vevőkészülék létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="0c00f-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="0c00f-121">A parancs új SMS-vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="0c00f-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="0c00f-122">3. példa: új webhook-vevőkészülék létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="0c00f-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="0c00f-123">A parancs új webhook-vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="0c00f-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="0c00f-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0c00f-124">PARAMETERS</span></span>

### <span data-ttu-id="0c00f-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="0c00f-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="0c00f-126">ArmRoleReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="0c00f-126">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="0c00f-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="0c00f-127">-AutomationAccountId</span></span>
<span data-ttu-id="0c00f-128">a AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="0c00f-128">the AutomationAccountId</span></span>

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

### <span data-ttu-id="0c00f-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="0c00f-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="0c00f-130">AutomationRunbookReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="0c00f-130">Create a AutomationRunbookReceiver</span></span>

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

### <span data-ttu-id="0c00f-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="0c00f-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="0c00f-132">az URI, ahová a webakasztókat el kell küldeni</span><span class="sxs-lookup"><span data-stu-id="0c00f-132">the URI where webhooks should be sent</span></span>

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

### <span data-ttu-id="0c00f-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="0c00f-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="0c00f-134">a AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="0c00f-134">the AzureAppPushEmailAddress</span></span>

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

### <span data-ttu-id="0c00f-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="0c00f-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="0c00f-136">AzureAppPushReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="0c00f-136">Create a AzureAppPushReceiver</span></span>

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

### <span data-ttu-id="0c00f-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="0c00f-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="0c00f-138">ArmRoleReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="0c00f-138">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="0c00f-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="0c00f-139">-CallbackUrl</span></span>
<span data-ttu-id="0c00f-140">a CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="0c00f-140">the CallbackUrl</span></span>

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

### <span data-ttu-id="0c00f-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="0c00f-141">-ConnectionId</span></span>
<span data-ttu-id="0c00f-142">a vevőkészülék ITSM-kapcsolat azonosítója</span><span class="sxs-lookup"><span data-stu-id="0c00f-142">the itsm connection id of this receiver</span></span>

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

### <span data-ttu-id="0c00f-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="0c00f-143">-CountryCode</span></span>
<span data-ttu-id="0c00f-144">Az SMS-vevőkészülék országkódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c00f-144">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="0c00f-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c00f-145">-DefaultProfile</span></span>
<span data-ttu-id="0c00f-146">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0c00f-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c00f-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="0c00f-147">-EmailAddress</span></span>
<span data-ttu-id="0c00f-148">Az E-mail címzett címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c00f-148">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="0c00f-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="0c00f-149">-EmailReceiver</span></span>
<span data-ttu-id="0c00f-150">E-mail-címzett létrehozásának megadása</span><span class="sxs-lookup"><span data-stu-id="0c00f-150">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="0c00f-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="0c00f-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="0c00f-152">a Function app resourceId</span><span class="sxs-lookup"><span data-stu-id="0c00f-152">the function app resourceId</span></span>

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

### <span data-ttu-id="0c00f-153">-Függvénynév</span><span class="sxs-lookup"><span data-stu-id="0c00f-153">-FunctionName</span></span>
<span data-ttu-id="0c00f-154">a függvénynév</span><span class="sxs-lookup"><span data-stu-id="0c00f-154">the functionName</span></span>

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

### <span data-ttu-id="0c00f-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="0c00f-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="0c00f-156">a httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="0c00f-156">the httpTriggerUrl</span></span>

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

### <span data-ttu-id="0c00f-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="0c00f-157">-IdentifierUri</span></span>
<span data-ttu-id="0c00f-158">az aad-hitelesítés azonosítójának URI azonosítója</span><span class="sxs-lookup"><span data-stu-id="0c00f-158">the Identifier uri for aad auth</span></span>

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

### <span data-ttu-id="0c00f-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="0c00f-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="0c00f-160">annak jelzése, hogy a példány globális runbook-e</span><span class="sxs-lookup"><span data-stu-id="0c00f-160">indicating whether this instance is global runbook</span></span>

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

### <span data-ttu-id="0c00f-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="0c00f-161">-ItsmReceiver</span></span>
<span data-ttu-id="0c00f-162">ItsmReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="0c00f-162">Create a ItsmReceiver</span></span>

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

### <span data-ttu-id="0c00f-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="0c00f-163">-LogicAppReceiver</span></span>
<span data-ttu-id="0c00f-164">LogicAppReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="0c00f-164">Create a LogicAppReceiver</span></span>

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

### <span data-ttu-id="0c00f-165">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0c00f-165">-Name</span></span>
<span data-ttu-id="0c00f-166">A címzett nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c00f-166">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="0c00f-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0c00f-167">-ObjectId</span></span>
<span data-ttu-id="0c00f-168">a aad Auth webhook app Object ID</span><span class="sxs-lookup"><span data-stu-id="0c00f-168">the webhook app object Id for aad auth</span></span>

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

### <span data-ttu-id="0c00f-169">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="0c00f-169">-PhoneNumber</span></span>
<span data-ttu-id="0c00f-170">Az SMS-vevőkészülék telefonszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c00f-170">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="0c00f-171">-Region (régió)</span><span class="sxs-lookup"><span data-stu-id="0c00f-171">-Region</span></span>
<span data-ttu-id="0c00f-172">a vevőkészülék ITSM területe</span><span class="sxs-lookup"><span data-stu-id="0c00f-172">the itsm Region of this receiver</span></span>

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

### <span data-ttu-id="0c00f-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c00f-173">-ResourceId</span></span>
<span data-ttu-id="0c00f-174">a ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c00f-174">the ResourceId</span></span>

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

### <span data-ttu-id="0c00f-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="0c00f-175">-RoleId</span></span>
<span data-ttu-id="0c00f-176">A vevőkészülék kar szerepkör-azonosítója</span><span class="sxs-lookup"><span data-stu-id="0c00f-176">The arm role id of the receiver</span></span>

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

### <span data-ttu-id="0c00f-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="0c00f-177">-RunbookName</span></span>
<span data-ttu-id="0c00f-178">a RunbookName</span><span class="sxs-lookup"><span data-stu-id="0c00f-178">the RunbookName</span></span>

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

### <span data-ttu-id="0c00f-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="0c00f-179">-ServiceUri</span></span>
<span data-ttu-id="0c00f-180">A webhook-vevőkészülék URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c00f-180">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="0c00f-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="0c00f-181">-SmsReceiver</span></span>
<span data-ttu-id="0c00f-182">Az SMS-vevőkészülék létrehozásának megadása</span><span class="sxs-lookup"><span data-stu-id="0c00f-182">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="0c00f-183">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="0c00f-183">-TenantId</span></span>
<span data-ttu-id="0c00f-184">a aad-hitelesítés bérlői azonosítója</span><span class="sxs-lookup"><span data-stu-id="0c00f-184">the tenant id for aad auth</span></span>

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

### <span data-ttu-id="0c00f-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c00f-185">-TicketConfiguration</span></span>
<span data-ttu-id="0c00f-186">a vevőkészülék ITSM TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c00f-186">the itsm TicketConfiguration of this receiver</span></span>

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

### <span data-ttu-id="0c00f-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="0c00f-187">-UseAadAuth</span></span>
<span data-ttu-id="0c00f-188">az Add Authentication bővítmény használatára szolgáló jelölő</span><span class="sxs-lookup"><span data-stu-id="0c00f-188">the flag to use add auth</span></span>

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

### <span data-ttu-id="0c00f-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="0c00f-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="0c00f-190">A megjelölés a gyakori riasztási sémát használja-e.</span><span class="sxs-lookup"><span data-stu-id="0c00f-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="0c00f-191">Ezt az értéket az neglectedfor SMS, Azure app push, ITSM és Voice recievers fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="0c00f-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

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

### <span data-ttu-id="0c00f-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="0c00f-192">-VoiceCountryCode</span></span>
<span data-ttu-id="0c00f-193">A hangvevőkészülék országkódot</span><span class="sxs-lookup"><span data-stu-id="0c00f-193">The country code of the voice receiver</span></span>

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

### <span data-ttu-id="0c00f-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="0c00f-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="0c00f-195">A hangvevőkészülék telefonszáma</span><span class="sxs-lookup"><span data-stu-id="0c00f-195">The phone number of the voice receiver</span></span>

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

### <span data-ttu-id="0c00f-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="0c00f-196">-VoiceReceiver</span></span>
<span data-ttu-id="0c00f-197">Hangvevőkészülék létrehozása</span><span class="sxs-lookup"><span data-stu-id="0c00f-197">Create a voice receiver</span></span>

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

### <span data-ttu-id="0c00f-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="0c00f-198">-WebhookReceiver</span></span>
<span data-ttu-id="0c00f-199">A webhook-vevőkészülék létrehozásának meghatározása</span><span class="sxs-lookup"><span data-stu-id="0c00f-199">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="0c00f-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="0c00f-200">-WebhookResourceId</span></span>
<span data-ttu-id="0c00f-201">a WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="0c00f-201">the WebhookResourceId</span></span>

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

### <span data-ttu-id="0c00f-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="0c00f-202">-WorkspaceId</span></span>
<span data-ttu-id="0c00f-203">a vevőkészülék ITSM munkaterület-azonosítója</span><span class="sxs-lookup"><span data-stu-id="0c00f-203">the itsm workspace id of this receiver</span></span>

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

### <span data-ttu-id="0c00f-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c00f-204">CommonParameters</span></span>
<span data-ttu-id="0c00f-205">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0c00f-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c00f-206">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0c00f-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c00f-207">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c00f-207">INPUTS</span></span>

### <span data-ttu-id="0c00f-208">System. String</span><span class="sxs-lookup"><span data-stu-id="0c00f-208">System.String</span></span>

### <span data-ttu-id="0c00f-209">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0c00f-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0c00f-210">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c00f-210">OUTPUTS</span></span>

### <span data-ttu-id="0c00f-211">Microsoft. Azure. commands. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="0c00f-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="0c00f-212">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0c00f-212">NOTES</span></span>

## <span data-ttu-id="0c00f-213">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c00f-213">RELATED LINKS</span></span>

<span data-ttu-id="0c00f-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="0c00f-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
