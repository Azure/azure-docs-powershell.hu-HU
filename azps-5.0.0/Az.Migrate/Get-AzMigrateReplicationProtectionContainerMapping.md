---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: e321691106d892c703a56bd94c3fe84ab7d9fe38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195774"
---
# <span data-ttu-id="f989a-101">Get-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="f989a-101">Get-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="f989a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f989a-102">SYNOPSIS</span></span>
<span data-ttu-id="f989a-103">A védelmi tárolók megfeleltetésének részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f989a-103">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="f989a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f989a-104">SYNTAX</span></span>

### <span data-ttu-id="f989a-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f989a-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f989a-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="f989a-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f989a-107">Lista</span><span class="sxs-lookup"><span data-stu-id="f989a-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f989a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f989a-108">DESCRIPTION</span></span>
<span data-ttu-id="f989a-109">A védelmi tárolók megfeleltetésének részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f989a-109">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="f989a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f989a-110">EXAMPLES</span></span>

### <span data-ttu-id="f989a-111">Példa 1: konkrét megfeleltetés beszerzése</span><span class="sxs-lookup"><span data-stu-id="f989a-111">Example 1: Get a specific mapping</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer -MappingName "containermapping"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="f989a-112">Megfeleltetési adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="f989a-112">Get a mapping detail.</span></span>

## <span data-ttu-id="f989a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f989a-113">PARAMETERS</span></span>

### <span data-ttu-id="f989a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f989a-114">-DefaultProfile</span></span>
<span data-ttu-id="f989a-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f989a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f989a-116">-FabricName</span><span class="sxs-lookup"><span data-stu-id="f989a-116">-FabricName</span></span>
<span data-ttu-id="f989a-117">A szövet neve.</span><span class="sxs-lookup"><span data-stu-id="f989a-117">Fabric name.</span></span>

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

### <span data-ttu-id="f989a-118">-MappingName</span><span class="sxs-lookup"><span data-stu-id="f989a-118">-MappingName</span></span>
<span data-ttu-id="f989a-119">Védelmi tároló megfeleltetésének neve.</span><span class="sxs-lookup"><span data-stu-id="f989a-119">Protection Container mapping name.</span></span>

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

### <span data-ttu-id="f989a-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="f989a-120">-ProtectionContainerName</span></span>
<span data-ttu-id="f989a-121">Védelmi tároló neve.</span><span class="sxs-lookup"><span data-stu-id="f989a-121">Protection container name.</span></span>

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

### <span data-ttu-id="f989a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f989a-122">-ResourceGroupName</span></span>
<span data-ttu-id="f989a-123">Annak az erőforráscsoportnek a neve, amelyben a helyreállítási szolgáltatások boltozata található.</span><span class="sxs-lookup"><span data-stu-id="f989a-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="f989a-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f989a-124">-ResourceName</span></span>
<span data-ttu-id="f989a-125">A helyreállítási szolgáltatások boltozatának neve.</span><span class="sxs-lookup"><span data-stu-id="f989a-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="f989a-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f989a-126">-SubscriptionId</span></span>
<span data-ttu-id="f989a-127">Az előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="f989a-127">The subscription Id.</span></span>

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

### <span data-ttu-id="f989a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f989a-128">CommonParameters</span></span>
<span data-ttu-id="f989a-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f989a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f989a-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f989a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f989a-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f989a-131">INPUTS</span></span>

## <span data-ttu-id="f989a-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f989a-132">OUTPUTS</span></span>

### <span data-ttu-id="f989a-133">Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api20180110. IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="f989a-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="f989a-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f989a-134">NOTES</span></span>

<span data-ttu-id="f989a-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f989a-135">ALIASES</span></span>

## <span data-ttu-id="f989a-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f989a-136">RELATED LINKS</span></span>

