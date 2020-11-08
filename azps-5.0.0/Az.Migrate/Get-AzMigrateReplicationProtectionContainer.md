---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
ms.openlocfilehash: a89d762f0317075a0da94290ad964aeef133fdd5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195777"
---
# <span data-ttu-id="96af0-101">Get-AzMigrateReplicationProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="96af0-101">Get-AzMigrateReplicationProtectionContainer</span></span>

## <span data-ttu-id="96af0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96af0-102">SYNOPSIS</span></span>
<span data-ttu-id="96af0-103">A védelmi tároló részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="96af0-103">Gets the details of a protection container.</span></span>

## <span data-ttu-id="96af0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96af0-104">SYNTAX</span></span>

### <span data-ttu-id="96af0-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="96af0-105">List (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainer -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="96af0-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="96af0-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="96af0-107">Lista1</span><span class="sxs-lookup"><span data-stu-id="96af0-107">List1</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ResourceGroupName <String>
 -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="96af0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="96af0-108">DESCRIPTION</span></span>
<span data-ttu-id="96af0-109">A védelmi tároló részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="96af0-109">Gets the details of a protection container.</span></span>

## <span data-ttu-id="96af0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="96af0-110">EXAMPLES</span></span>

### <span data-ttu-id="96af0-111">1. példa: az összes védett tároló felsorolása a boltozaton és a szöveten</span><span class="sxs-lookup"><span data-stu-id="96af0-111">Example 1: List all protection containers in vault and fabric</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="96af0-112">Az összes listázása.</span><span class="sxs-lookup"><span data-stu-id="96af0-112">Lists all.</span></span>

### <span data-ttu-id="96af0-113">2. példa: adott tároló beszerzése</span><span class="sxs-lookup"><span data-stu-id="96af0-113">Example 2: Get a specific container</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="96af0-114">Egy adott személy beolvasása</span><span class="sxs-lookup"><span data-stu-id="96af0-114">Gets a specific one.</span></span>

## <span data-ttu-id="96af0-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96af0-115">PARAMETERS</span></span>

### <span data-ttu-id="96af0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96af0-116">-DefaultProfile</span></span>
<span data-ttu-id="96af0-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96af0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96af0-118">-FabricName</span><span class="sxs-lookup"><span data-stu-id="96af0-118">-FabricName</span></span>
<span data-ttu-id="96af0-119">A szövet neve.</span><span class="sxs-lookup"><span data-stu-id="96af0-119">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96af0-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="96af0-120">-ProtectionContainerName</span></span>
<span data-ttu-id="96af0-121">Védelmi tároló neve.</span><span class="sxs-lookup"><span data-stu-id="96af0-121">Protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96af0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96af0-122">-ResourceGroupName</span></span>
<span data-ttu-id="96af0-123">Annak az erőforráscsoportnek a neve, amelyben a helyreállítási szolgáltatások boltozata található.</span><span class="sxs-lookup"><span data-stu-id="96af0-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="96af0-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="96af0-124">-ResourceName</span></span>
<span data-ttu-id="96af0-125">A helyreállítási szolgáltatások boltozatának neve.</span><span class="sxs-lookup"><span data-stu-id="96af0-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="96af0-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96af0-126">-SubscriptionId</span></span>
<span data-ttu-id="96af0-127">Az előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="96af0-127">The subscription Id.</span></span>

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

### <span data-ttu-id="96af0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96af0-128">CommonParameters</span></span>
<span data-ttu-id="96af0-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96af0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96af0-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="96af0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96af0-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96af0-131">INPUTS</span></span>

## <span data-ttu-id="96af0-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96af0-132">OUTPUTS</span></span>

### <span data-ttu-id="96af0-133">Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api20180110. IProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="96af0-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span></span>

## <span data-ttu-id="96af0-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96af0-134">NOTES</span></span>

<span data-ttu-id="96af0-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="96af0-135">ALIASES</span></span>

## <span data-ttu-id="96af0-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96af0-136">RELATED LINKS</span></span>

