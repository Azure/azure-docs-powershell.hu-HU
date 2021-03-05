---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/new-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
ms.openlocfilehash: 11f3124c98e84dcaec40c3b8ecd9b8831b572617
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009301"
---
# <span data-ttu-id="82f01-101">New-AzBotService</span><span class="sxs-lookup"><span data-stu-id="82f01-101">New-AzBotService</span></span>

## <span data-ttu-id="82f01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82f01-102">SYNOPSIS</span></span>
<span data-ttu-id="82f01-103">A paraméterek által megadott BotService értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="82f01-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="82f01-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="82f01-104">SYNTAX</span></span>

### <span data-ttu-id="82f01-105">Regisztráció (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="82f01-105">Registration (Default)</span></span>
```
New-AzBotService -ApplicationId <String> -Location <String> [-BotTemplateType <String>]
 [-Description <String>] [-DisplayName <String>] [-Endpoint <String>] [-Language <String>] [-Name <String>]
 [-Registration] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="82f01-106">WebApp</span><span class="sxs-lookup"><span data-stu-id="82f01-106">WebApp</span></span>
```
New-AzBotService -ApplicationId <String> -ApplicationSecret <SecureString> -Location <String>
 [-BotTemplateType <String>] [-Description <String>] [-ExistingServerFarmId <String>] [-Language <String>]
 [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Webapp] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="82f01-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="82f01-107">DESCRIPTION</span></span>
<span data-ttu-id="82f01-108">A paraméterek által megadott BotService értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="82f01-108">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="82f01-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="82f01-109">EXAMPLES</span></span>

### <span data-ttu-id="82f01-110">1. példa: Új robot létrehozása</span><span class="sxs-lookup"><span data-stu-id="82f01-110">Example 1: Create a new bot</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-bot1 -ApplicationId "af5fce4d-ee68-4b25-be09-f3222582e133"-Location eastus -Sku F0 -Description "123134" -Registration

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="82f01-111">Új robot létrehozása ResourceGroupName és ApplicationId szerint</span><span class="sxs-lookup"><span data-stu-id="82f01-111">Create a new Bot by ResourceGroupName and ApplicationId</span></span>

### <span data-ttu-id="82f01-112">2. példa: Új webalkalmazás létrehozása</span><span class="sxs-lookup"><span data-stu-id="82f01-112">Example 2: Create a new Web App</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-apptest14 -ApplicationId "b1ab1727-0465-4255-a1bb-976210af972c" -Location eastus -Sku F0 -Description "123134" -Webapp

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest14 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="82f01-113">Új webalkalmazás létrehozása a ResourceGroupName és az ApplicationId alapján</span><span class="sxs-lookup"><span data-stu-id="82f01-113">Create a new Web App by ResourceGroupName and ApplicationId</span></span>

## <span data-ttu-id="82f01-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82f01-114">PARAMETERS</span></span>

### <span data-ttu-id="82f01-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="82f01-115">-ApplicationId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f01-116">-ApplicationSecret</span><span class="sxs-lookup"><span data-stu-id="82f01-116">-ApplicationSecret</span></span>


```yaml
Type: System.Security.SecureString
Parameter Sets: WebApp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f01-117">-BotTemplateType</span><span class="sxs-lookup"><span data-stu-id="82f01-117">-BotTemplateType</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f01-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82f01-118">-DefaultProfile</span></span>
<span data-ttu-id="82f01-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82f01-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f01-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="82f01-120">-Description</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f01-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="82f01-121">-DisplayName</span></span>


```yaml
Type: System.String
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f01-122">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="82f01-122">-Endpoint</span></span>


```yaml
Type: System.String
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f01-123">-ExistingServerFarmId</span><span class="sxs-lookup"><span data-stu-id="82f01-123">-ExistingServerFarmId</span></span>


```yaml
Type: System.String
Parameter Sets: WebApp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f01-124">-Language</span><span class="sxs-lookup"><span data-stu-id="82f01-124">-Language</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f01-125">-Location</span><span class="sxs-lookup"><span data-stu-id="82f01-125">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f01-126">-Name</span><span class="sxs-lookup"><span data-stu-id="82f01-126">-Name</span></span>
<span data-ttu-id="82f01-127">A roboterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="82f01-127">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f01-128">-Regisztráció</span><span class="sxs-lookup"><span data-stu-id="82f01-128">-Registration</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f01-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82f01-129">-ResourceGroupName</span></span>
<span data-ttu-id="82f01-130">A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="82f01-130">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f01-131">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="82f01-131">-Sku</span></span>
<span data-ttu-id="82f01-132">A termékváltozat neve</span><span class="sxs-lookup"><span data-stu-id="82f01-132">The sku name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f01-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="82f01-133">-SubscriptionId</span></span>
<span data-ttu-id="82f01-134">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="82f01-134">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f01-135">-Webapp</span><span class="sxs-lookup"><span data-stu-id="82f01-135">-Webapp</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebApp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f01-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82f01-136">CommonParameters</span></span>
<span data-ttu-id="82f01-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82f01-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82f01-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82f01-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82f01-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82f01-139">INPUTS</span></span>

## <span data-ttu-id="82f01-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82f01-140">OUTPUTS</span></span>

### <span data-ttu-id="82f01-141">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="82f01-141">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="82f01-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="82f01-142">NOTES</span></span>

<span data-ttu-id="82f01-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="82f01-143">ALIASES</span></span>

## <span data-ttu-id="82f01-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82f01-144">RELATED LINKS</span></span>

