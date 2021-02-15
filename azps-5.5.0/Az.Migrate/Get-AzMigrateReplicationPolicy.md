---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: e2cad9282e1e662cee58625a17c3f0672947d26a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157403"
---
# <span data-ttu-id="a2c56-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="a2c56-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="a2c56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2c56-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c56-103">A replikációs házirend részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="a2c56-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="a2c56-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a2c56-104">SYNTAX</span></span>

### <span data-ttu-id="a2c56-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2c56-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a2c56-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="a2c56-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a2c56-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a2c56-107">DESCRIPTION</span></span>
<span data-ttu-id="a2c56-108">A replikációs házirend részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="a2c56-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="a2c56-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a2c56-109">EXAMPLES</span></span>

### <span data-ttu-id="a2c56-110">1. példa: Az összes házirend lekérte egy tárolóba</span><span class="sxs-lookup"><span data-stu-id="a2c56-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="a2c56-111">Szerezze be az összes házirendet.</span><span class="sxs-lookup"><span data-stu-id="a2c56-111">Get all policies.</span></span>

### <span data-ttu-id="a2c56-112">2. példa: Adott házirend lekérte</span><span class="sxs-lookup"><span data-stu-id="a2c56-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="a2c56-113">Konkrét adatok lekérte.</span><span class="sxs-lookup"><span data-stu-id="a2c56-113">Get a specific one.</span></span>

## <span data-ttu-id="a2c56-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2c56-114">PARAMETERS</span></span>

### <span data-ttu-id="a2c56-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c56-115">-DefaultProfile</span></span>
<span data-ttu-id="a2c56-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2c56-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2c56-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="a2c56-117">-PolicyName</span></span>
<span data-ttu-id="a2c56-118">Replikációs házirend neve.</span><span class="sxs-lookup"><span data-stu-id="a2c56-118">Replication policy name.</span></span>

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

### <span data-ttu-id="a2c56-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2c56-119">-ResourceGroupName</span></span>
<span data-ttu-id="a2c56-120">Annak az erőforráscsoportnak a neve, amelyben a helyreállítási szolgáltatások tárolója jelen van.</span><span class="sxs-lookup"><span data-stu-id="a2c56-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="a2c56-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a2c56-121">-ResourceName</span></span>
<span data-ttu-id="a2c56-122">A helyreállítási szolgáltatások tárolója neve.</span><span class="sxs-lookup"><span data-stu-id="a2c56-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="a2c56-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2c56-123">-SubscriptionId</span></span>
<span data-ttu-id="a2c56-124">Azure-előfizetés azonosítója, amelyben a projekt létrejött.</span><span class="sxs-lookup"><span data-stu-id="a2c56-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="a2c56-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c56-125">CommonParameters</span></span>
<span data-ttu-id="a2c56-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2c56-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c56-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2c56-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c56-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2c56-128">INPUTS</span></span>

## <span data-ttu-id="a2c56-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2c56-129">OUTPUTS</span></span>

### <span data-ttu-id="a2c56-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span><span class="sxs-lookup"><span data-stu-id="a2c56-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="a2c56-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a2c56-131">NOTES</span></span>

<span data-ttu-id="a2c56-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a2c56-132">ALIASES</span></span>

## <span data-ttu-id="a2c56-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2c56-133">RELATED LINKS</span></span>

