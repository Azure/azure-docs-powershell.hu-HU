---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/new-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
ms.openlocfilehash: 4e40665e4fdb7332865342132982d6d598bd8d30
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478049"
---
# <span data-ttu-id="92a74-101">New-AzBotService</span><span class="sxs-lookup"><span data-stu-id="92a74-101">New-AzBotService</span></span>

## <span data-ttu-id="92a74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92a74-102">SYNOPSIS</span></span>
<span data-ttu-id="92a74-103">A paraméterek által megadott BotService értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="92a74-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="92a74-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="92a74-104">SYNTAX</span></span>

### <span data-ttu-id="92a74-105">Regisztráció (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="92a74-105">Registration (Default)</span></span>
```
New-AzBotService -ApplicationId <String> -Location <String> [-BotTemplateType <String>]
 [-Description <String>] [-DisplayName <String>] [-Endpoint <String>] [-Language <String>] [-Name <String>]
 [-Registration] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="92a74-106">WebApp</span><span class="sxs-lookup"><span data-stu-id="92a74-106">WebApp</span></span>
```
New-AzBotService -ApplicationId <String> -ApplicationSecret <SecureString> -Location <String>
 [-BotTemplateType <String>] [-Description <String>] [-ExistingServerFarmId <String>] [-Language <String>]
 [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Webapp] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="92a74-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="92a74-107">DESCRIPTION</span></span>
<span data-ttu-id="92a74-108">A paraméterek által megadott BotService értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="92a74-108">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="92a74-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="92a74-109">EXAMPLES</span></span>

### <span data-ttu-id="92a74-110">1. példa: Új robot létrehozása</span><span class="sxs-lookup"><span data-stu-id="92a74-110">Example 1: Create a new bot</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-bot1 -ApplicationId "af5fce4d-ee68-4b25-be09-f3222582e133"-Location eastus -Sku F0 -Description "123134" -Registration

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="92a74-111">Új robot létrehozása ResourceGroupName és ApplicationId szerint</span><span class="sxs-lookup"><span data-stu-id="92a74-111">Create a new Bot by ResourceGroupName and ApplicationId</span></span>

### <span data-ttu-id="92a74-112">2. példa: Új webalkalmazás létrehozása</span><span class="sxs-lookup"><span data-stu-id="92a74-112">Example 2: Create a new Web App</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-apptest14 -ApplicationId "b1ab1727-0465-4255-a1bb-976210af972c" -Location eastus -Sku F0 -Description "123134" -Webapp

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest14 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="92a74-113">Új webalkalmazás létrehozása a ResourceGroupName és az ApplicationId alapján</span><span class="sxs-lookup"><span data-stu-id="92a74-113">Create a new Web App by ResourceGroupName and ApplicationId</span></span>

## <span data-ttu-id="92a74-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92a74-114">PARAMETERS</span></span>

### <span data-ttu-id="92a74-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="92a74-115">-ApplicationId</span></span>


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

### <span data-ttu-id="92a74-116">-ApplicationSecret</span><span class="sxs-lookup"><span data-stu-id="92a74-116">-ApplicationSecret</span></span>


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

### <span data-ttu-id="92a74-117">-BotTemplateType</span><span class="sxs-lookup"><span data-stu-id="92a74-117">-BotTemplateType</span></span>


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

### <span data-ttu-id="92a74-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92a74-118">-DefaultProfile</span></span>
<span data-ttu-id="92a74-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92a74-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92a74-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="92a74-120">-Description</span></span>


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

### <span data-ttu-id="92a74-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="92a74-121">-DisplayName</span></span>


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

### <span data-ttu-id="92a74-122">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="92a74-122">-Endpoint</span></span>


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

### <span data-ttu-id="92a74-123">-ExistingServerFarmId</span><span class="sxs-lookup"><span data-stu-id="92a74-123">-ExistingServerFarmId</span></span>


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

### <span data-ttu-id="92a74-124">-Language</span><span class="sxs-lookup"><span data-stu-id="92a74-124">-Language</span></span>


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

### <span data-ttu-id="92a74-125">-Location</span><span class="sxs-lookup"><span data-stu-id="92a74-125">-Location</span></span>


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

### <span data-ttu-id="92a74-126">-Name</span><span class="sxs-lookup"><span data-stu-id="92a74-126">-Name</span></span>
<span data-ttu-id="92a74-127">A roboterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="92a74-127">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="92a74-128">-Regisztráció</span><span class="sxs-lookup"><span data-stu-id="92a74-128">-Registration</span></span>


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

### <span data-ttu-id="92a74-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92a74-129">-ResourceGroupName</span></span>
<span data-ttu-id="92a74-130">A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="92a74-130">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="92a74-131">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="92a74-131">-Sku</span></span>
<span data-ttu-id="92a74-132">A termékváltozat neve</span><span class="sxs-lookup"><span data-stu-id="92a74-132">The sku name</span></span>

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

### <span data-ttu-id="92a74-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92a74-133">-SubscriptionId</span></span>
<span data-ttu-id="92a74-134">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="92a74-134">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="92a74-135">-Webapp</span><span class="sxs-lookup"><span data-stu-id="92a74-135">-Webapp</span></span>


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

### <span data-ttu-id="92a74-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92a74-136">CommonParameters</span></span>
<span data-ttu-id="92a74-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92a74-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92a74-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92a74-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92a74-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92a74-139">INPUTS</span></span>

## <span data-ttu-id="92a74-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92a74-140">OUTPUTS</span></span>

### <span data-ttu-id="92a74-141">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="92a74-141">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="92a74-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="92a74-142">NOTES</span></span>

<span data-ttu-id="92a74-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="92a74-143">ALIASES</span></span>

## <span data-ttu-id="92a74-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92a74-144">RELATED LINKS</span></span>

