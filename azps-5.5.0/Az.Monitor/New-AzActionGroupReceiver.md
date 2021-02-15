---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: f2862c08212f5e41de10cb600edb22c38eac68d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159442"
---
# <span data-ttu-id="b8c25-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="b8c25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8c25-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c25-103">Létrehoz egy új műveletcsoport-fogadót.</span><span class="sxs-lookup"><span data-stu-id="b8c25-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="b8c25-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b8c25-104">SYNTAX</span></span>

### <span data-ttu-id="b8c25-105">NewEmailReceiver (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b8c25-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8c25-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8c25-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8c25-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8c25-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8c25-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8c25-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8c25-112">NewAppReceiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8c25-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8c25-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8c25-115">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b8c25-115">DESCRIPTION</span></span>
<span data-ttu-id="b8c25-116">A **New-AzActionGroupReceiver** parancsmag új műveletcsoport-fogadót hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="b8c25-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="b8c25-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b8c25-117">EXAMPLES</span></span>

### <span data-ttu-id="b8c25-118">1. példa: Új e-mail-fogadó létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="b8c25-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="b8c25-119">Ez a parancs új e-mail-fogadót hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="b8c25-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="b8c25-120">2. példa: Hozzon létre egy új SMS-fogadót a memóriában.</span><span class="sxs-lookup"><span data-stu-id="b8c25-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="b8c25-121">Ez a parancs új SMS-fogadót hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="b8c25-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="b8c25-122">3. példa: Hozzon létre egy új webhook-fogadót a memóriában.</span><span class="sxs-lookup"><span data-stu-id="b8c25-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="b8c25-123">Ez a parancs egy új webhook-vevőt hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="b8c25-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="b8c25-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8c25-124">PARAMETERS</span></span>

### <span data-ttu-id="b8c25-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="b8c25-126">ArmRoleReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="b8c25-126">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="b8c25-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="b8c25-127">-AutomationAccountId</span></span>
<span data-ttu-id="b8c25-128">the AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="b8c25-128">the AutomationAccountId</span></span>

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

### <span data-ttu-id="b8c25-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="b8c25-130">AutomationRunbookReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="b8c25-130">Create a AutomationRunbookReceiver</span></span>

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

### <span data-ttu-id="b8c25-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="b8c25-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="b8c25-132">az URI, ahová a webhookokat el kell küldeni</span><span class="sxs-lookup"><span data-stu-id="b8c25-132">the URI where webhooks should be sent</span></span>

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

### <span data-ttu-id="b8c25-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="b8c25-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="b8c25-134">the AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="b8c25-134">the AzureAppPushEmailAddress</span></span>

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

### <span data-ttu-id="b8c25-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="b8c25-136">AzureAppPushReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="b8c25-136">Create a AzureAppPushReceiver</span></span>

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

### <span data-ttu-id="b8c25-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="b8c25-138">ArmRoleReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="b8c25-138">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="b8c25-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="b8c25-139">-CallbackUrl</span></span>
<span data-ttu-id="b8c25-140">the CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="b8c25-140">the CallbackUrl</span></span>

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

### <span data-ttu-id="b8c25-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="b8c25-141">-ConnectionId</span></span>
<span data-ttu-id="b8c25-142">the itsm connection id of this receiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-142">the itsm connection id of this receiver</span></span>

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

### <span data-ttu-id="b8c25-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="b8c25-143">-CountryCode</span></span>
<span data-ttu-id="b8c25-144">Az SMS-fogadó országkódját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8c25-144">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="b8c25-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c25-145">-DefaultProfile</span></span>
<span data-ttu-id="b8c25-146">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b8c25-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8c25-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="b8c25-147">-EmailAddress</span></span>
<span data-ttu-id="b8c25-148">Az e-mail-fogadó címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8c25-148">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="b8c25-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-149">-EmailReceiver</span></span>
<span data-ttu-id="b8c25-150">E-mail-fogadó létrehozása</span><span class="sxs-lookup"><span data-stu-id="b8c25-150">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="b8c25-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="b8c25-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="b8c25-152">the function app resourceId</span><span class="sxs-lookup"><span data-stu-id="b8c25-152">the function app resourceId</span></span>

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

### <span data-ttu-id="b8c25-153">-FunctionName</span><span class="sxs-lookup"><span data-stu-id="b8c25-153">-FunctionName</span></span>
<span data-ttu-id="b8c25-154">the functionName</span><span class="sxs-lookup"><span data-stu-id="b8c25-154">the functionName</span></span>

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

### <span data-ttu-id="b8c25-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="b8c25-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="b8c25-156">the httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="b8c25-156">the httpTriggerUrl</span></span>

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

### <span data-ttu-id="b8c25-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="b8c25-157">-IdentifierUri</span></span>
<span data-ttu-id="b8c25-158">the Identifier uri for aad auth</span><span class="sxs-lookup"><span data-stu-id="b8c25-158">the Identifier uri for aad auth</span></span>

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

### <span data-ttu-id="b8c25-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="b8c25-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="b8c25-160">annak jelzése, hogy ez a példány globális runbook-e</span><span class="sxs-lookup"><span data-stu-id="b8c25-160">indicating whether this instance is global runbook</span></span>

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

### <span data-ttu-id="b8c25-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-161">-ItsmReceiver</span></span>
<span data-ttu-id="b8c25-162">ItsmReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="b8c25-162">Create a ItsmReceiver</span></span>

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

### <span data-ttu-id="b8c25-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-163">-LogicAppReceiver</span></span>
<span data-ttu-id="b8c25-164">LogicAppReceiver létrehozása</span><span class="sxs-lookup"><span data-stu-id="b8c25-164">Create a LogicAppReceiver</span></span>

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

### <span data-ttu-id="b8c25-165">-Name</span><span class="sxs-lookup"><span data-stu-id="b8c25-165">-Name</span></span>
<span data-ttu-id="b8c25-166">A fogadó neve.</span><span class="sxs-lookup"><span data-stu-id="b8c25-166">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="b8c25-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b8c25-167">-ObjectId</span></span>
<span data-ttu-id="b8c25-168">the webhook app object Id for aad auth</span><span class="sxs-lookup"><span data-stu-id="b8c25-168">the webhook app object Id for aad auth</span></span>

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

### <span data-ttu-id="b8c25-169">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="b8c25-169">-PhoneNumber</span></span>
<span data-ttu-id="b8c25-170">Az SMS-fogadó telefonszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8c25-170">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="b8c25-171">-Régió</span><span class="sxs-lookup"><span data-stu-id="b8c25-171">-Region</span></span>
<span data-ttu-id="b8c25-172">the itsm Region of this receiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-172">the itsm Region of this receiver</span></span>

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

### <span data-ttu-id="b8c25-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8c25-173">-ResourceId</span></span>
<span data-ttu-id="b8c25-174">the ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8c25-174">the ResourceId</span></span>

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

### <span data-ttu-id="b8c25-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="b8c25-175">-RoleId</span></span>
<span data-ttu-id="b8c25-176">A fogadókar szerepkörazonosítója</span><span class="sxs-lookup"><span data-stu-id="b8c25-176">The arm role id of the receiver</span></span>

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

### <span data-ttu-id="b8c25-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="b8c25-177">-RunbookName</span></span>
<span data-ttu-id="b8c25-178">the RunbookName</span><span class="sxs-lookup"><span data-stu-id="b8c25-178">the RunbookName</span></span>

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

### <span data-ttu-id="b8c25-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="b8c25-179">-ServiceUri</span></span>
<span data-ttu-id="b8c25-180">A webhook-fogadó URI-ját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8c25-180">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="b8c25-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-181">-SmsReceiver</span></span>
<span data-ttu-id="b8c25-182">AZT adja meg, hogy létre kell hoznia egy SMS-fogadót</span><span class="sxs-lookup"><span data-stu-id="b8c25-182">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="b8c25-183">-TenantId</span><span class="sxs-lookup"><span data-stu-id="b8c25-183">-TenantId</span></span>
<span data-ttu-id="b8c25-184">the tenant id for aad auth</span><span class="sxs-lookup"><span data-stu-id="b8c25-184">the tenant id for aad auth</span></span>

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

### <span data-ttu-id="b8c25-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8c25-185">-TicketConfiguration</span></span>
<span data-ttu-id="b8c25-186">the itsm TicketConfiguration of this receiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-186">the itsm TicketConfiguration of this receiver</span></span>

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

### <span data-ttu-id="b8c25-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="b8c25-187">-UseAadAuth</span></span>
<span data-ttu-id="b8c25-188">the flag to use add auth</span><span class="sxs-lookup"><span data-stu-id="b8c25-188">the flag to use add auth</span></span>

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

### <span data-ttu-id="b8c25-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="b8c25-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="b8c25-190">A jelző, amely jelzi, hogy a gyakori riasztási sémát kell-e használni.</span><span class="sxs-lookup"><span data-stu-id="b8c25-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="b8c25-191">Ezt az értéket figyelmen kívül fogjuk hagyva az SMS- és Azure App-leküldés, az ITSM és a Voice recievers miatt.</span><span class="sxs-lookup"><span data-stu-id="b8c25-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

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

### <span data-ttu-id="b8c25-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="b8c25-192">-VoiceCountryCode</span></span>
<span data-ttu-id="b8c25-193">A hangkagyló országkódja</span><span class="sxs-lookup"><span data-stu-id="b8c25-193">The country code of the voice receiver</span></span>

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

### <span data-ttu-id="b8c25-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="b8c25-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="b8c25-195">A hangkagyló telefonszáma</span><span class="sxs-lookup"><span data-stu-id="b8c25-195">The phone number of the voice receiver</span></span>

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

### <span data-ttu-id="b8c25-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-196">-VoiceReceiver</span></span>
<span data-ttu-id="b8c25-197">Hangkagyló létrehozása</span><span class="sxs-lookup"><span data-stu-id="b8c25-197">Create a voice receiver</span></span>

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

### <span data-ttu-id="b8c25-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-198">-WebhookReceiver</span></span>
<span data-ttu-id="b8c25-199">Webhook-fogadó létrehozása</span><span class="sxs-lookup"><span data-stu-id="b8c25-199">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="b8c25-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="b8c25-200">-WebhookResourceId</span></span>
<span data-ttu-id="b8c25-201">the WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="b8c25-201">the WebhookResourceId</span></span>

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

### <span data-ttu-id="b8c25-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="b8c25-202">-WorkspaceId</span></span>
<span data-ttu-id="b8c25-203">the itsm workspace id of this receiver</span><span class="sxs-lookup"><span data-stu-id="b8c25-203">the itsm workspace id of this receiver</span></span>

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

### <span data-ttu-id="b8c25-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c25-204">CommonParameters</span></span>
<span data-ttu-id="b8c25-205">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8c25-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c25-206">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8c25-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c25-207">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8c25-207">INPUTS</span></span>

### <span data-ttu-id="b8c25-208">System.String</span><span class="sxs-lookup"><span data-stu-id="b8c25-208">System.String</span></span>

### <span data-ttu-id="b8c25-209">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b8c25-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b8c25-210">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8c25-210">OUTPUTS</span></span>

### <span data-ttu-id="b8c25-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="b8c25-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="b8c25-212">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b8c25-212">NOTES</span></span>

## <span data-ttu-id="b8c25-213">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8c25-213">RELATED LINKS</span></span>

<span data-ttu-id="b8c25-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="b8c25-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
