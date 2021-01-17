---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: a5e35096966355a69ad5b363b61ab3cd5d2f0d0b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342834"
---
# <span data-ttu-id="c9561-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="c9561-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="c9561-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9561-102">SYNOPSIS</span></span>
<span data-ttu-id="c9561-103">A replikációs házirend részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="c9561-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="c9561-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c9561-104">SYNTAX</span></span>

### <span data-ttu-id="c9561-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c9561-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9561-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="c9561-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c9561-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c9561-107">DESCRIPTION</span></span>
<span data-ttu-id="c9561-108">A replikációs házirend részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="c9561-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="c9561-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c9561-109">EXAMPLES</span></span>

### <span data-ttu-id="c9561-110">1. példa: Az összes házirend lekérte egy tárolóba</span><span class="sxs-lookup"><span data-stu-id="c9561-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="c9561-111">Szerezze be az összes házirendet.</span><span class="sxs-lookup"><span data-stu-id="c9561-111">Get all policies.</span></span>

### <span data-ttu-id="c9561-112">2. példa: Adott házirend lekérte</span><span class="sxs-lookup"><span data-stu-id="c9561-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="c9561-113">Egy konkrétat is lekért.</span><span class="sxs-lookup"><span data-stu-id="c9561-113">Get a specific one.</span></span>

## <span data-ttu-id="c9561-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9561-114">PARAMETERS</span></span>

### <span data-ttu-id="c9561-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9561-115">-DefaultProfile</span></span>
<span data-ttu-id="c9561-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9561-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9561-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="c9561-117">-PolicyName</span></span>
<span data-ttu-id="c9561-118">Replikációs házirend neve.</span><span class="sxs-lookup"><span data-stu-id="c9561-118">Replication policy name.</span></span>

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

### <span data-ttu-id="c9561-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9561-119">-ResourceGroupName</span></span>
<span data-ttu-id="c9561-120">Annak az erőforráscsoportnak a neve, amelyben a helyreállítási szolgáltatások tárolója jelen van.</span><span class="sxs-lookup"><span data-stu-id="c9561-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="c9561-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c9561-121">-ResourceName</span></span>
<span data-ttu-id="c9561-122">A helyreállítási szolgáltatások tárolója neve.</span><span class="sxs-lookup"><span data-stu-id="c9561-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="c9561-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c9561-123">-SubscriptionId</span></span>
<span data-ttu-id="c9561-124">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c9561-124">The subscription Id.</span></span>

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

### <span data-ttu-id="c9561-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9561-125">CommonParameters</span></span>
<span data-ttu-id="c9561-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9561-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9561-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9561-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9561-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9561-128">INPUTS</span></span>

## <span data-ttu-id="c9561-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9561-129">OUTPUTS</span></span>

### <span data-ttu-id="c9561-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span><span class="sxs-lookup"><span data-stu-id="c9561-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="c9561-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c9561-131">NOTES</span></span>

<span data-ttu-id="c9561-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c9561-132">ALIASES</span></span>

## <span data-ttu-id="c9561-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9561-133">RELATED LINKS</span></span>

