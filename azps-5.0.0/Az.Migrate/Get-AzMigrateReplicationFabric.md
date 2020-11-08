---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 8230056069668765d3d27a9dd54538a310edf383
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195779"
---
# <span data-ttu-id="0571c-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="0571c-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="0571c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0571c-102">SYNOPSIS</span></span>
<span data-ttu-id="0571c-103">Egy Azure webhely-helyreállítási anyag adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0571c-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="0571c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0571c-104">SYNTAX</span></span>

### <span data-ttu-id="0571c-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0571c-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0571c-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="0571c-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0571c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0571c-107">DESCRIPTION</span></span>
<span data-ttu-id="0571c-108">Egy Azure webhely-helyreállítási anyag adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0571c-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="0571c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0571c-109">EXAMPLES</span></span>

### <span data-ttu-id="0571c-110">Példa 1: az összes anyag beolvasása erőforráscsoport szerint és a boltozat neve</span><span class="sxs-lookup"><span data-stu-id="0571c-110">Example 1: Get all fabrics by resource group and vault name</span></span>
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

<span data-ttu-id="0571c-111">A teljes anyag kinyerése az erőforráscsoport és a boltozat csoportban</span><span class="sxs-lookup"><span data-stu-id="0571c-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="0571c-112">2. példa: az anyag beolvasása erőforráscsoport szerint, a boltozat neve és a szövet neve</span><span class="sxs-lookup"><span data-stu-id="0571c-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
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

<span data-ttu-id="0571c-113">Speciális anyag beszerzése</span><span class="sxs-lookup"><span data-stu-id="0571c-113">Get a specific fabric</span></span>

## <span data-ttu-id="0571c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0571c-114">PARAMETERS</span></span>

### <span data-ttu-id="0571c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0571c-115">-DefaultProfile</span></span>
<span data-ttu-id="0571c-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0571c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0571c-117">-FabricName</span><span class="sxs-lookup"><span data-stu-id="0571c-117">-FabricName</span></span>
<span data-ttu-id="0571c-118">A szövet neve.</span><span class="sxs-lookup"><span data-stu-id="0571c-118">Fabric name.</span></span>

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

### <span data-ttu-id="0571c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0571c-119">-ResourceGroupName</span></span>
<span data-ttu-id="0571c-120">Annak az erőforráscsoportnek a neve, amelyben a helyreállítási szolgáltatások boltozata található.</span><span class="sxs-lookup"><span data-stu-id="0571c-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="0571c-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0571c-121">-ResourceName</span></span>
<span data-ttu-id="0571c-122">A helyreállítási szolgáltatások boltozatának neve.</span><span class="sxs-lookup"><span data-stu-id="0571c-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="0571c-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0571c-123">-SubscriptionId</span></span>
<span data-ttu-id="0571c-124">Az előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="0571c-124">The subscription Id.</span></span>

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

### <span data-ttu-id="0571c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0571c-125">CommonParameters</span></span>
<span data-ttu-id="0571c-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0571c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0571c-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0571c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0571c-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0571c-128">INPUTS</span></span>

## <span data-ttu-id="0571c-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0571c-129">OUTPUTS</span></span>

### <span data-ttu-id="0571c-130">Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api20180110. IFabric</span><span class="sxs-lookup"><span data-stu-id="0571c-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="0571c-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0571c-131">NOTES</span></span>

<span data-ttu-id="0571c-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0571c-132">ALIASES</span></span>

## <span data-ttu-id="0571c-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0571c-133">RELATED LINKS</span></span>

