---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: a5e35096966355a69ad5b363b61ab3cd5d2f0d0b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195778"
---
# <span data-ttu-id="f09d7-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="f09d7-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="f09d7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f09d7-102">SYNOPSIS</span></span>
<span data-ttu-id="f09d7-103">A replikációs házirend részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f09d7-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="f09d7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f09d7-104">SYNTAX</span></span>

### <span data-ttu-id="f09d7-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f09d7-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f09d7-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="f09d7-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f09d7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f09d7-107">DESCRIPTION</span></span>
<span data-ttu-id="f09d7-108">A replikációs házirend részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f09d7-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="f09d7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f09d7-109">EXAMPLES</span></span>

### <span data-ttu-id="f09d7-110">Példa 1: az összes házirend beolvasása egy boltozatban</span><span class="sxs-lookup"><span data-stu-id="f09d7-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="f09d7-111">Minden házirend beszerzése.</span><span class="sxs-lookup"><span data-stu-id="f09d7-111">Get all policies.</span></span>

### <span data-ttu-id="f09d7-112">2. példa: speciális házirend beszerzése</span><span class="sxs-lookup"><span data-stu-id="f09d7-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="f09d7-113">Szerezzen be egy konkrétt.</span><span class="sxs-lookup"><span data-stu-id="f09d7-113">Get a specific one.</span></span>

## <span data-ttu-id="f09d7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f09d7-114">PARAMETERS</span></span>

### <span data-ttu-id="f09d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f09d7-115">-DefaultProfile</span></span>
<span data-ttu-id="f09d7-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f09d7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f09d7-117">-Házirendnév</span><span class="sxs-lookup"><span data-stu-id="f09d7-117">-PolicyName</span></span>
<span data-ttu-id="f09d7-118">Replikációs házirend neve.</span><span class="sxs-lookup"><span data-stu-id="f09d7-118">Replication policy name.</span></span>

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

### <span data-ttu-id="f09d7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f09d7-119">-ResourceGroupName</span></span>
<span data-ttu-id="f09d7-120">Annak az erőforráscsoportnek a neve, amelyben a helyreállítási szolgáltatások boltozata található.</span><span class="sxs-lookup"><span data-stu-id="f09d7-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="f09d7-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f09d7-121">-ResourceName</span></span>
<span data-ttu-id="f09d7-122">A helyreállítási szolgáltatások boltozatának neve.</span><span class="sxs-lookup"><span data-stu-id="f09d7-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="f09d7-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f09d7-123">-SubscriptionId</span></span>
<span data-ttu-id="f09d7-124">Az előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="f09d7-124">The subscription Id.</span></span>

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

### <span data-ttu-id="f09d7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f09d7-125">CommonParameters</span></span>
<span data-ttu-id="f09d7-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f09d7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f09d7-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f09d7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f09d7-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f09d7-128">INPUTS</span></span>

## <span data-ttu-id="f09d7-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f09d7-129">OUTPUTS</span></span>

### <span data-ttu-id="f09d7-130">Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api20180110. IPolicy</span><span class="sxs-lookup"><span data-stu-id="f09d7-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="f09d7-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f09d7-131">NOTES</span></span>

<span data-ttu-id="f09d7-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f09d7-132">ALIASES</span></span>

## <span data-ttu-id="f09d7-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f09d7-133">RELATED LINKS</span></span>

