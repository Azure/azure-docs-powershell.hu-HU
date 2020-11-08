---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: f2862c08212f5e41de10cb600edb22c38eac68d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195745"
---
# <span data-ttu-id="f1a06-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="f1a06-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="f1a06-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1a06-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a06-103">Új akciócsoport-vevőkészülék létrehozása.</span><span class="sxs-lookup"><span data-stu-id="f1a06-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="f1a06-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1a06-104">SYNTAX</span></span>

### <span data-ttu-id="f1a06-105">NewEmailReceiver (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f1a06-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1a06-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="f1a06-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1a06-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="f1a06-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1a06-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="f1a06-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1a06-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="f1a06-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1a06-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="f1a06-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1a06-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="f1a06-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1a06-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="f1a06-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1a06-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="f1a06-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1a06-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="f1a06-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1a06-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1a06-115">DESCRIPTION</span></span>
<span data-ttu-id="f1a06-116">A **New-AzActionGroupReceiver** parancsmag új műveleti csoportba foglalt vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="f1a06-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="f1a06-117">Példák</span><span class="sxs-lookup"><span data-stu-id="f1a06-117">EXAMPLES</span></span>

### <span data-ttu-id="f1a06-118">Példa 1: új e-mail-vevőkészülék létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="f1a06-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="f1a06-119">A parancs új e-mail-vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="f1a06-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="f1a06-120">2. példa: új SMS-vevőkészülék létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="f1a06-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="f1a06-121">A parancs új SMS-vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="f1a06-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="f1a06-122">3. példa: új webhook-vevőkészülék létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="f1a06-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="f1a06-123">A parancs új webhook-vevőkészüléket hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="f1a06-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="f1a06-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1a06-124">PARAMETERS</span></span>

### <span data-ttu-id="f1a06-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="f1a06-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="f1a06-126">ArmRoleReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="f1a06-126">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="f1a06-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="f1a06-127">-AutomationAccountId</span></span>
<span data-ttu-id="f1a06-128">a AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="f1a06-128">the AutomationAccountId</span></span>

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

### <span data-ttu-id="f1a06-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="f1a06-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="f1a06-130">AutomationRunbookReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="f1a06-130">Create a AutomationRunbookReceiver</span></span>

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

### <span data-ttu-id="f1a06-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="f1a06-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="f1a06-132">az URI, ahová a webakasztókat el kell küldeni</span><span class="sxs-lookup"><span data-stu-id="f1a06-132">the URI where webhooks should be sent</span></span>

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

### <span data-ttu-id="f1a06-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f1a06-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="f1a06-134">a AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f1a06-134">the AzureAppPushEmailAddress</span></span>

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

### <span data-ttu-id="f1a06-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="f1a06-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="f1a06-136">AzureAppPushReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="f1a06-136">Create a AzureAppPushReceiver</span></span>

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

### <span data-ttu-id="f1a06-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="f1a06-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="f1a06-138">ArmRoleReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="f1a06-138">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="f1a06-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="f1a06-139">-CallbackUrl</span></span>
<span data-ttu-id="f1a06-140">a CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="f1a06-140">the CallbackUrl</span></span>

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

### <span data-ttu-id="f1a06-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="f1a06-141">-ConnectionId</span></span>
<span data-ttu-id="f1a06-142">a vevőkészülék ITSM-kapcsolat azonosítója</span><span class="sxs-lookup"><span data-stu-id="f1a06-142">the itsm connection id of this receiver</span></span>

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

### <span data-ttu-id="f1a06-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="f1a06-143">-CountryCode</span></span>
<span data-ttu-id="f1a06-144">Az SMS-vevőkészülék országkódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1a06-144">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="f1a06-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a06-145">-DefaultProfile</span></span>
<span data-ttu-id="f1a06-146">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f1a06-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1a06-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="f1a06-147">-EmailAddress</span></span>
<span data-ttu-id="f1a06-148">Az E-mail címzett címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1a06-148">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="f1a06-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="f1a06-149">-EmailReceiver</span></span>
<span data-ttu-id="f1a06-150">E-mail-címzett létrehozásának megadása</span><span class="sxs-lookup"><span data-stu-id="f1a06-150">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="f1a06-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="f1a06-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="f1a06-152">a Function app resourceId</span><span class="sxs-lookup"><span data-stu-id="f1a06-152">the function app resourceId</span></span>

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

### <span data-ttu-id="f1a06-153">-Függvénynév</span><span class="sxs-lookup"><span data-stu-id="f1a06-153">-FunctionName</span></span>
<span data-ttu-id="f1a06-154">a függvénynév</span><span class="sxs-lookup"><span data-stu-id="f1a06-154">the functionName</span></span>

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

### <span data-ttu-id="f1a06-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="f1a06-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="f1a06-156">a httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="f1a06-156">the httpTriggerUrl</span></span>

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

### <span data-ttu-id="f1a06-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="f1a06-157">-IdentifierUri</span></span>
<span data-ttu-id="f1a06-158">az aad-hitelesítés azonosítójának URI azonosítója</span><span class="sxs-lookup"><span data-stu-id="f1a06-158">the Identifier uri for aad auth</span></span>

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

### <span data-ttu-id="f1a06-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="f1a06-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="f1a06-160">annak jelzése, hogy a példány globális runbook-e</span><span class="sxs-lookup"><span data-stu-id="f1a06-160">indicating whether this instance is global runbook</span></span>

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

### <span data-ttu-id="f1a06-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="f1a06-161">-ItsmReceiver</span></span>
<span data-ttu-id="f1a06-162">ItsmReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="f1a06-162">Create a ItsmReceiver</span></span>

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

### <span data-ttu-id="f1a06-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="f1a06-163">-LogicAppReceiver</span></span>
<span data-ttu-id="f1a06-164">LogicAppReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="f1a06-164">Create a LogicAppReceiver</span></span>

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

### <span data-ttu-id="f1a06-165">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f1a06-165">-Name</span></span>
<span data-ttu-id="f1a06-166">A címzett nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1a06-166">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="f1a06-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f1a06-167">-ObjectId</span></span>
<span data-ttu-id="f1a06-168">a aad Auth webhook app Object ID</span><span class="sxs-lookup"><span data-stu-id="f1a06-168">the webhook app object Id for aad auth</span></span>

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

### <span data-ttu-id="f1a06-169">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="f1a06-169">-PhoneNumber</span></span>
<span data-ttu-id="f1a06-170">Az SMS-vevőkészülék telefonszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1a06-170">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="f1a06-171">-Region (régió)</span><span class="sxs-lookup"><span data-stu-id="f1a06-171">-Region</span></span>
<span data-ttu-id="f1a06-172">a vevőkészülék ITSM területe</span><span class="sxs-lookup"><span data-stu-id="f1a06-172">the itsm Region of this receiver</span></span>

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

### <span data-ttu-id="f1a06-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1a06-173">-ResourceId</span></span>
<span data-ttu-id="f1a06-174">a ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1a06-174">the ResourceId</span></span>

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

### <span data-ttu-id="f1a06-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="f1a06-175">-RoleId</span></span>
<span data-ttu-id="f1a06-176">A vevőkészülék kar szerepkör-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f1a06-176">The arm role id of the receiver</span></span>

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

### <span data-ttu-id="f1a06-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="f1a06-177">-RunbookName</span></span>
<span data-ttu-id="f1a06-178">a RunbookName</span><span class="sxs-lookup"><span data-stu-id="f1a06-178">the RunbookName</span></span>

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

### <span data-ttu-id="f1a06-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="f1a06-179">-ServiceUri</span></span>
<span data-ttu-id="f1a06-180">A webhook-vevőkészülék URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1a06-180">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="f1a06-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="f1a06-181">-SmsReceiver</span></span>
<span data-ttu-id="f1a06-182">Az SMS-vevőkészülék létrehozásának megadása</span><span class="sxs-lookup"><span data-stu-id="f1a06-182">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="f1a06-183">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="f1a06-183">-TenantId</span></span>
<span data-ttu-id="f1a06-184">a aad-hitelesítés bérlői azonosítója</span><span class="sxs-lookup"><span data-stu-id="f1a06-184">the tenant id for aad auth</span></span>

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

### <span data-ttu-id="f1a06-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1a06-185">-TicketConfiguration</span></span>
<span data-ttu-id="f1a06-186">a vevőkészülék ITSM TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1a06-186">the itsm TicketConfiguration of this receiver</span></span>

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

### <span data-ttu-id="f1a06-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="f1a06-187">-UseAadAuth</span></span>
<span data-ttu-id="f1a06-188">az Add Authentication bővítmény használatára szolgáló jelölő</span><span class="sxs-lookup"><span data-stu-id="f1a06-188">the flag to use add auth</span></span>

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

### <span data-ttu-id="f1a06-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="f1a06-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="f1a06-190">A megjelölés a gyakori riasztási sémát használja-e.</span><span class="sxs-lookup"><span data-stu-id="f1a06-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="f1a06-191">Ezt az értéket az neglectedfor SMS, Azure app push, ITSM és Voice recievers fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="f1a06-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

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

### <span data-ttu-id="f1a06-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="f1a06-192">-VoiceCountryCode</span></span>
<span data-ttu-id="f1a06-193">A hangvevőkészülék országkódot</span><span class="sxs-lookup"><span data-stu-id="f1a06-193">The country code of the voice receiver</span></span>

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

### <span data-ttu-id="f1a06-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="f1a06-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="f1a06-195">A hangvevőkészülék telefonszáma</span><span class="sxs-lookup"><span data-stu-id="f1a06-195">The phone number of the voice receiver</span></span>

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

### <span data-ttu-id="f1a06-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="f1a06-196">-VoiceReceiver</span></span>
<span data-ttu-id="f1a06-197">Hangvevőkészülék létrehozása</span><span class="sxs-lookup"><span data-stu-id="f1a06-197">Create a voice receiver</span></span>

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

### <span data-ttu-id="f1a06-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="f1a06-198">-WebhookReceiver</span></span>
<span data-ttu-id="f1a06-199">A webhook-vevőkészülék létrehozásának meghatározása</span><span class="sxs-lookup"><span data-stu-id="f1a06-199">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="f1a06-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="f1a06-200">-WebhookResourceId</span></span>
<span data-ttu-id="f1a06-201">a WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="f1a06-201">the WebhookResourceId</span></span>

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

### <span data-ttu-id="f1a06-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="f1a06-202">-WorkspaceId</span></span>
<span data-ttu-id="f1a06-203">a vevőkészülék ITSM munkaterület-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f1a06-203">the itsm workspace id of this receiver</span></span>

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

### <span data-ttu-id="f1a06-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a06-204">CommonParameters</span></span>
<span data-ttu-id="f1a06-205">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1a06-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a06-206">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f1a06-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a06-207">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1a06-207">INPUTS</span></span>

### <span data-ttu-id="f1a06-208">System. String</span><span class="sxs-lookup"><span data-stu-id="f1a06-208">System.String</span></span>

### <span data-ttu-id="f1a06-209">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f1a06-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f1a06-210">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1a06-210">OUTPUTS</span></span>

### <span data-ttu-id="f1a06-211">Microsoft. Azure. commands. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="f1a06-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="f1a06-212">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1a06-212">NOTES</span></span>

## <span data-ttu-id="f1a06-213">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1a06-213">RELATED LINKS</span></span>

<span data-ttu-id="f1a06-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="f1a06-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>