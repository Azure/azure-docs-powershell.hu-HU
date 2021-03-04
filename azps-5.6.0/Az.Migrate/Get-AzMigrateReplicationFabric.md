---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 25106d6facb65346360bf7c78b7cbef27fc9a517
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934082"
---
# <span data-ttu-id="c85cd-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="c85cd-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="c85cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c85cd-102">SYNOPSIS</span></span>
<span data-ttu-id="c85cd-103">Az Azure Webhely-helyreállítási szerkezet részleteinek leszerzése.</span><span class="sxs-lookup"><span data-stu-id="c85cd-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="c85cd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c85cd-104">SYNTAX</span></span>

### <span data-ttu-id="c85cd-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c85cd-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c85cd-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="c85cd-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c85cd-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c85cd-107">DESCRIPTION</span></span>
<span data-ttu-id="c85cd-108">Az Azure Webhely-helyreállítási szerkezet részleteinek leszerzése.</span><span class="sxs-lookup"><span data-stu-id="c85cd-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="c85cd-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c85cd-109">EXAMPLES</span></span>

### <span data-ttu-id="c85cd-110">1. példa: Az összes anyag behozása erőforráscsoport és tárolónév szerint</span><span class="sxs-lookup"><span data-stu-id="c85cd-110">Example 1: Get all fabrics by resource group and vault name</span></span>
```powershell
PS C:\> PS Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="c85cd-111">Az összes anyag behozása az erőforráscsoportba és a tárolóba</span><span class="sxs-lookup"><span data-stu-id="c85cd-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="c85cd-112">2. példa: Anyag behozása erőforráscsoportok, tárolónév és anyagnév szerint</span><span class="sxs-lookup"><span data-stu-id="c85cd-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="c85cd-113">Speciális anyag behozatk</span><span class="sxs-lookup"><span data-stu-id="c85cd-113">Get a specific fabric</span></span>

## <span data-ttu-id="c85cd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c85cd-114">PARAMETERS</span></span>

### <span data-ttu-id="c85cd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c85cd-115">-DefaultProfile</span></span>
<span data-ttu-id="c85cd-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c85cd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c85cd-117">-FabricName</span><span class="sxs-lookup"><span data-stu-id="c85cd-117">-FabricName</span></span>
<span data-ttu-id="c85cd-118">Anyagnév.</span><span class="sxs-lookup"><span data-stu-id="c85cd-118">Fabric name.</span></span>

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

### <span data-ttu-id="c85cd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c85cd-119">-ResourceGroupName</span></span>
<span data-ttu-id="c85cd-120">Annak az erőforráscsoportnak a neve, amelyben a helyreállítási szolgáltatások tárolója jelen van.</span><span class="sxs-lookup"><span data-stu-id="c85cd-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="c85cd-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c85cd-121">-ResourceName</span></span>
<span data-ttu-id="c85cd-122">A helyreállítási szolgáltatások tárolója neve.</span><span class="sxs-lookup"><span data-stu-id="c85cd-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="c85cd-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c85cd-123">-SubscriptionId</span></span>
<span data-ttu-id="c85cd-124">Azure-előfizetés azonosítója, amelyben a projekt létrejött.</span><span class="sxs-lookup"><span data-stu-id="c85cd-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="c85cd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c85cd-125">CommonParameters</span></span>
<span data-ttu-id="c85cd-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c85cd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c85cd-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c85cd-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c85cd-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c85cd-128">INPUTS</span></span>

## <span data-ttu-id="c85cd-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c85cd-129">OUTPUTS</span></span>

### <span data-ttu-id="c85cd-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span><span class="sxs-lookup"><span data-stu-id="c85cd-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="c85cd-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c85cd-131">NOTES</span></span>

<span data-ttu-id="c85cd-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c85cd-132">ALIASES</span></span>

## <span data-ttu-id="c85cd-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c85cd-133">RELATED LINKS</span></span>

