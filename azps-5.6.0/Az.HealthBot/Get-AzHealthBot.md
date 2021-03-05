---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/get-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
ms.openlocfilehash: 1e9360c7545b1a8c566e1a373b8650e6b6800323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013237"
---
# <span data-ttu-id="313c1-101">Get-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="313c1-101">Get-AzHealthBot</span></span>

## <span data-ttu-id="313c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="313c1-102">SYNOPSIS</span></span>
<span data-ttu-id="313c1-103">Szerezze be a HealthBotot.</span><span class="sxs-lookup"><span data-stu-id="313c1-103">Get a HealthBot.</span></span>

## <span data-ttu-id="313c1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="313c1-104">SYNTAX</span></span>

### <span data-ttu-id="313c1-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="313c1-105">List1 (Default)</span></span>
```
Get-AzHealthBot [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="313c1-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="313c1-106">Get</span></span>
```
Get-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="313c1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="313c1-107">GetViaIdentity</span></span>
```
Get-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="313c1-108">Lista</span><span class="sxs-lookup"><span data-stu-id="313c1-108">List</span></span>
```
Get-AzHealthBot -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="313c1-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="313c1-109">DESCRIPTION</span></span>
<span data-ttu-id="313c1-110">Szerezze be a HealthBotot.</span><span class="sxs-lookup"><span data-stu-id="313c1-110">Get a HealthBot.</span></span>

## <span data-ttu-id="313c1-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="313c1-111">EXAMPLES</span></span>

### <span data-ttu-id="313c1-112">1. példa: Az összes HealthBot lekérte</span><span class="sxs-lookup"><span data-stu-id="313c1-112">Example 1: Get all HealthBot</span></span>
```powershell
PS C:\> Get-AzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="313c1-113">Az összes HealthBot lekérte</span><span class="sxs-lookup"><span data-stu-id="313c1-113">Get all HealthBot</span></span>

### <span data-ttu-id="313c1-114">2. példa: Az összes HealthBot lekérte a ResourceGroupName szerint</span><span class="sxs-lookup"><span data-stu-id="313c1-114">Example 2: Get all HealthBot by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="313c1-115">Az összes HealthBot lekérte: ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="313c1-115">Get all HealthBot by ResourceGroupName</span></span>

### <span data-ttu-id="313c1-116">3. példa: A HealthBot lekérte resourcegroupname és name szerint</span><span class="sxs-lookup"><span data-stu-id="313c1-116">Example 3: Get HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="313c1-117">Get HealthBot by ResourceGroupName and Name</span><span class="sxs-lookup"><span data-stu-id="313c1-117">Get HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="313c1-118">4. példa: A HealthBot lekérte az InputObject eszközét</span><span class="sxs-lookup"><span data-stu-id="313c1-118">Example 4: Get HealthBot by InputObject</span></span>
```powershell
PS C:\> $getAzHealthBot = Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot
Get-AzHealthBot -InputObject $getAzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="313c1-119">A HealthBot lekérte az InputObject eszközét</span><span class="sxs-lookup"><span data-stu-id="313c1-119">Get HealthBot by InputObject</span></span>

## <span data-ttu-id="313c1-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="313c1-120">PARAMETERS</span></span>

### <span data-ttu-id="313c1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="313c1-121">-DefaultProfile</span></span>
<span data-ttu-id="313c1-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="313c1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="313c1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="313c1-123">-InputObject</span></span>
<span data-ttu-id="313c1-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="313c1-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="313c1-125">-Name</span><span class="sxs-lookup"><span data-stu-id="313c1-125">-Name</span></span>
<span data-ttu-id="313c1-126">A roboterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="313c1-126">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="313c1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="313c1-127">-ResourceGroupName</span></span>
<span data-ttu-id="313c1-128">A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="313c1-128">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="313c1-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="313c1-129">-SubscriptionId</span></span>
<span data-ttu-id="313c1-130">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="313c1-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="313c1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="313c1-131">CommonParameters</span></span>
<span data-ttu-id="313c1-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="313c1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="313c1-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="313c1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="313c1-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="313c1-134">INPUTS</span></span>

### <span data-ttu-id="313c1-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="313c1-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="313c1-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="313c1-136">OUTPUTS</span></span>

### <span data-ttu-id="313c1-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="313c1-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="313c1-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="313c1-138">NOTES</span></span>

<span data-ttu-id="313c1-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="313c1-139">ALIASES</span></span>

<span data-ttu-id="313c1-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="313c1-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="313c1-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="313c1-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="313c1-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="313c1-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="313c1-143">INPUTOBJECT: <IHealthBotIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="313c1-143">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="313c1-144">`[BotName <String>]`: A roboterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="313c1-144">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="313c1-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="313c1-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="313c1-146">`[ResourceGroupName <String>]`: A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="313c1-146">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="313c1-147">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="313c1-147">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="313c1-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="313c1-148">RELATED LINKS</span></span>

