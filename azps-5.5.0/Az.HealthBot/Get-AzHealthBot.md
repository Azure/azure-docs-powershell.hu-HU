---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthbot/get-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
ms.openlocfilehash: f7e1f596aef9169a1238f505d39f0dd201dcd8bb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147811"
---
# <span data-ttu-id="01357-101">Get-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="01357-101">Get-AzHealthBot</span></span>

## <span data-ttu-id="01357-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01357-102">SYNOPSIS</span></span>
<span data-ttu-id="01357-103">Szerezze be a HealthBotot.</span><span class="sxs-lookup"><span data-stu-id="01357-103">Get a HealthBot.</span></span>

## <span data-ttu-id="01357-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="01357-104">SYNTAX</span></span>

### <span data-ttu-id="01357-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="01357-105">List1 (Default)</span></span>
```
Get-AzHealthBot [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="01357-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="01357-106">Get</span></span>
```
Get-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="01357-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="01357-107">GetViaIdentity</span></span>
```
Get-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="01357-108">Lista</span><span class="sxs-lookup"><span data-stu-id="01357-108">List</span></span>
```
Get-AzHealthBot -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="01357-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="01357-109">DESCRIPTION</span></span>
<span data-ttu-id="01357-110">Szerezze be a HealthBotot.</span><span class="sxs-lookup"><span data-stu-id="01357-110">Get a HealthBot.</span></span>

## <span data-ttu-id="01357-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="01357-111">EXAMPLES</span></span>

### <span data-ttu-id="01357-112">1. példa: Az összes HealthBot lekérte</span><span class="sxs-lookup"><span data-stu-id="01357-112">Example 1: Get all HealthBot</span></span>
```powershell
PS C:\> Get-AzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="01357-113">Az összes HealthBot lekérte</span><span class="sxs-lookup"><span data-stu-id="01357-113">Get all HealthBot</span></span>

### <span data-ttu-id="01357-114">2. példa: Az összes HealthBot lekérte a ResourceGroupName szerint</span><span class="sxs-lookup"><span data-stu-id="01357-114">Example 2: Get all HealthBot by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="01357-115">Az összes HealthBot lekérte: ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01357-115">Get all HealthBot by ResourceGroupName</span></span>

### <span data-ttu-id="01357-116">3. példa: A HealthBot lekérte a ResourceGroupName és a Name nevet</span><span class="sxs-lookup"><span data-stu-id="01357-116">Example 3: Get HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="01357-117">Get HealthBot by ResourceGroupName and Name</span><span class="sxs-lookup"><span data-stu-id="01357-117">Get HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="01357-118">4. példa: A HealthBot lekérte az InputObject eszközét</span><span class="sxs-lookup"><span data-stu-id="01357-118">Example 4: Get HealthBot by InputObject</span></span>
```powershell
PS C:\> $getAzHealthBot = Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot
Get-AzHealthBot -InputObject $getAzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="01357-119">A HealthBot lekérte az InputObject eszközét</span><span class="sxs-lookup"><span data-stu-id="01357-119">Get HealthBot by InputObject</span></span>

## <span data-ttu-id="01357-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01357-120">PARAMETERS</span></span>

### <span data-ttu-id="01357-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01357-121">-DefaultProfile</span></span>
<span data-ttu-id="01357-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01357-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01357-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01357-123">-InputObject</span></span>
<span data-ttu-id="01357-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="01357-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="01357-125">-Name</span><span class="sxs-lookup"><span data-stu-id="01357-125">-Name</span></span>
<span data-ttu-id="01357-126">A roboterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="01357-126">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="01357-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01357-127">-ResourceGroupName</span></span>
<span data-ttu-id="01357-128">A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="01357-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="01357-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="01357-129">-SubscriptionId</span></span>
<span data-ttu-id="01357-130">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="01357-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="01357-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01357-131">CommonParameters</span></span>
<span data-ttu-id="01357-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01357-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01357-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01357-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01357-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01357-134">INPUTS</span></span>

### <span data-ttu-id="01357-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="01357-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="01357-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01357-136">OUTPUTS</span></span>

### <span data-ttu-id="01357-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="01357-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="01357-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="01357-138">NOTES</span></span>

<span data-ttu-id="01357-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="01357-139">ALIASES</span></span>

<span data-ttu-id="01357-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="01357-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="01357-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="01357-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="01357-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="01357-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="01357-143">INPUTOBJECT: <IHealthBotIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="01357-143">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="01357-144">`[BotName <String>]`: A roboterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="01357-144">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="01357-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="01357-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="01357-146">`[ResourceGroupName <String>]`: A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="01357-146">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="01357-147">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="01357-147">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="01357-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01357-148">RELATED LINKS</span></span>

