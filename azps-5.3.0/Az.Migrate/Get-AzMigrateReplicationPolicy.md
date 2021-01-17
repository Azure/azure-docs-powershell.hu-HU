---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: a5e35096966355a69ad5b363b61ab3cd5d2f0d0b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480055"
---
# <span data-ttu-id="380f4-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="380f4-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="380f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="380f4-102">SYNOPSIS</span></span>
<span data-ttu-id="380f4-103">A replikációs házirend részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="380f4-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="380f4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="380f4-104">SYNTAX</span></span>

### <span data-ttu-id="380f4-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="380f4-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="380f4-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="380f4-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="380f4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="380f4-107">DESCRIPTION</span></span>
<span data-ttu-id="380f4-108">A replikációs házirend részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="380f4-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="380f4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="380f4-109">EXAMPLES</span></span>

### <span data-ttu-id="380f4-110">1. példa: Az összes házirend lekérte egy tárolóba</span><span class="sxs-lookup"><span data-stu-id="380f4-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="380f4-111">Szerezze be az összes házirendet.</span><span class="sxs-lookup"><span data-stu-id="380f4-111">Get all policies.</span></span>

### <span data-ttu-id="380f4-112">2. példa: Adott házirend lekérte</span><span class="sxs-lookup"><span data-stu-id="380f4-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="380f4-113">Konkrét adatok lekérte.</span><span class="sxs-lookup"><span data-stu-id="380f4-113">Get a specific one.</span></span>

## <span data-ttu-id="380f4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="380f4-114">PARAMETERS</span></span>

### <span data-ttu-id="380f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="380f4-115">-DefaultProfile</span></span>
<span data-ttu-id="380f4-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="380f4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="380f4-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="380f4-117">-PolicyName</span></span>
<span data-ttu-id="380f4-118">Replikációs házirend neve.</span><span class="sxs-lookup"><span data-stu-id="380f4-118">Replication policy name.</span></span>

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

### <span data-ttu-id="380f4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="380f4-119">-ResourceGroupName</span></span>
<span data-ttu-id="380f4-120">Annak az erőforráscsoportnak a neve, amelyben a helyreállítási szolgáltatások tárolója jelen van.</span><span class="sxs-lookup"><span data-stu-id="380f4-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="380f4-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="380f4-121">-ResourceName</span></span>
<span data-ttu-id="380f4-122">A helyreállítási szolgáltatások tárolója neve.</span><span class="sxs-lookup"><span data-stu-id="380f4-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="380f4-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="380f4-123">-SubscriptionId</span></span>
<span data-ttu-id="380f4-124">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="380f4-124">The subscription Id.</span></span>

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

### <span data-ttu-id="380f4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="380f4-125">CommonParameters</span></span>
<span data-ttu-id="380f4-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="380f4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="380f4-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="380f4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="380f4-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="380f4-128">INPUTS</span></span>

## <span data-ttu-id="380f4-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="380f4-129">OUTPUTS</span></span>

### <span data-ttu-id="380f4-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span><span class="sxs-lookup"><span data-stu-id="380f4-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="380f4-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="380f4-131">NOTES</span></span>

<span data-ttu-id="380f4-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="380f4-132">ALIASES</span></span>

## <span data-ttu-id="380f4-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="380f4-133">RELATED LINKS</span></span>

