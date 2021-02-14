---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: e706e9eb21f601ed1a266faa0afb888297f17fdb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157387"
---
# <span data-ttu-id="5490e-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="5490e-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="5490e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5490e-102">SYNOPSIS</span></span>
<span data-ttu-id="5490e-103">A regisztrált helyreállítási szolgáltató adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="5490e-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="5490e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5490e-104">SYNTAX</span></span>

### <span data-ttu-id="5490e-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5490e-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5490e-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="5490e-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="5490e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5490e-107">DESCRIPTION</span></span>
<span data-ttu-id="5490e-108">A regisztrált helyreállítási szolgáltató adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="5490e-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="5490e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5490e-109">EXAMPLES</span></span>

### <span data-ttu-id="5490e-110">1. példa: Az összes szolgáltató behozatkja a tárolóba</span><span class="sxs-lookup"><span data-stu-id="5490e-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="5490e-111">Az összes felsorolása.</span><span class="sxs-lookup"><span data-stu-id="5490e-111">List all.</span></span>

## <span data-ttu-id="5490e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5490e-112">PARAMETERS</span></span>

### <span data-ttu-id="5490e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5490e-113">-DefaultProfile</span></span>
<span data-ttu-id="5490e-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5490e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5490e-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="5490e-115">-FabricName</span></span>
<span data-ttu-id="5490e-116">Anyagnév.</span><span class="sxs-lookup"><span data-stu-id="5490e-116">Fabric name.</span></span>

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

### <span data-ttu-id="5490e-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="5490e-117">-ProviderName</span></span>
<span data-ttu-id="5490e-118">Helyreállítási szolgáltatás szolgáltatójának neve</span><span class="sxs-lookup"><span data-stu-id="5490e-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="5490e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5490e-119">-ResourceGroupName</span></span>
<span data-ttu-id="5490e-120">Annak az erőforráscsoportnak a neve, amelyben a helyreállítási szolgáltatások tárolója jelen van.</span><span class="sxs-lookup"><span data-stu-id="5490e-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="5490e-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5490e-121">-ResourceName</span></span>
<span data-ttu-id="5490e-122">A helyreállítási szolgáltatások tárolója neve.</span><span class="sxs-lookup"><span data-stu-id="5490e-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="5490e-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5490e-123">-SubscriptionId</span></span>
<span data-ttu-id="5490e-124">Azure-előfizetés azonosítója, amelyben a projekt létrejött.</span><span class="sxs-lookup"><span data-stu-id="5490e-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="5490e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5490e-125">CommonParameters</span></span>
<span data-ttu-id="5490e-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5490e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5490e-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5490e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5490e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5490e-128">INPUTS</span></span>

## <span data-ttu-id="5490e-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5490e-129">OUTPUTS</span></span>

### <span data-ttu-id="5490e-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="5490e-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="5490e-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5490e-131">NOTES</span></span>

<span data-ttu-id="5490e-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="5490e-132">ALIASES</span></span>

## <span data-ttu-id="5490e-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5490e-133">RELATED LINKS</span></span>

