---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: fd9bfed884ba2480a797ec5f83f99913496638e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369947"
---
# <span data-ttu-id="ed930-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ed930-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="ed930-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed930-102">SYNOPSIS</span></span>
<span data-ttu-id="ed930-103">A regisztrált helyreállítási szolgáltató adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ed930-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="ed930-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ed930-104">SYNTAX</span></span>

### <span data-ttu-id="ed930-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ed930-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ed930-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="ed930-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed930-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ed930-107">DESCRIPTION</span></span>
<span data-ttu-id="ed930-108">A regisztrált helyreállítási szolgáltató adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ed930-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="ed930-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ed930-109">EXAMPLES</span></span>

### <span data-ttu-id="ed930-110">1. példa: Az összes szolgáltató behozatkja a tárolóba</span><span class="sxs-lookup"><span data-stu-id="ed930-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="ed930-111">Az összes felsorolása.</span><span class="sxs-lookup"><span data-stu-id="ed930-111">List all.</span></span>

## <span data-ttu-id="ed930-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed930-112">PARAMETERS</span></span>

### <span data-ttu-id="ed930-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed930-113">-DefaultProfile</span></span>
<span data-ttu-id="ed930-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed930-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed930-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="ed930-115">-FabricName</span></span>
<span data-ttu-id="ed930-116">Anyagnév.</span><span class="sxs-lookup"><span data-stu-id="ed930-116">Fabric name.</span></span>

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

### <span data-ttu-id="ed930-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="ed930-117">-ProviderName</span></span>
<span data-ttu-id="ed930-118">Helyreállítási szolgáltatás szolgáltatójának neve</span><span class="sxs-lookup"><span data-stu-id="ed930-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="ed930-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed930-119">-ResourceGroupName</span></span>
<span data-ttu-id="ed930-120">Annak az erőforráscsoportnak a neve, amelyben a helyreállítási szolgáltatások tárolója jelen van.</span><span class="sxs-lookup"><span data-stu-id="ed930-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="ed930-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ed930-121">-ResourceName</span></span>
<span data-ttu-id="ed930-122">A helyreállítási szolgáltatások tárolója neve.</span><span class="sxs-lookup"><span data-stu-id="ed930-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="ed930-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ed930-123">-SubscriptionId</span></span>
<span data-ttu-id="ed930-124">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ed930-124">The subscription Id.</span></span>

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

### <span data-ttu-id="ed930-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed930-125">CommonParameters</span></span>
<span data-ttu-id="ed930-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed930-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed930-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed930-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed930-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed930-128">INPUTS</span></span>

## <span data-ttu-id="ed930-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed930-129">OUTPUTS</span></span>

### <span data-ttu-id="ed930-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ed930-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="ed930-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ed930-131">NOTES</span></span>

<span data-ttu-id="ed930-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ed930-132">ALIASES</span></span>

## <span data-ttu-id="ed930-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed930-133">RELATED LINKS</span></span>

