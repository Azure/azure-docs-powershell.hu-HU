---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: fd9bfed884ba2480a797ec5f83f99913496638e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195771"
---
# <span data-ttu-id="26597-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="26597-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="26597-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26597-102">SYNOPSIS</span></span>
<span data-ttu-id="26597-103">A regisztrált helyreállítási szolgáltatások szolgáltatójának adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="26597-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="26597-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26597-104">SYNTAX</span></span>

### <span data-ttu-id="26597-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="26597-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="26597-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="26597-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="26597-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="26597-107">DESCRIPTION</span></span>
<span data-ttu-id="26597-108">A regisztrált helyreállítási szolgáltatások szolgáltatójának adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="26597-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="26597-109">Példák</span><span class="sxs-lookup"><span data-stu-id="26597-109">EXAMPLES</span></span>

### <span data-ttu-id="26597-110">Példa 1: az összes szolgáltató beszerzése a Vault-ban</span><span class="sxs-lookup"><span data-stu-id="26597-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="26597-111">Az összes listázása.</span><span class="sxs-lookup"><span data-stu-id="26597-111">List all.</span></span>

## <span data-ttu-id="26597-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26597-112">PARAMETERS</span></span>

### <span data-ttu-id="26597-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26597-113">-DefaultProfile</span></span>
<span data-ttu-id="26597-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26597-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26597-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="26597-115">-FabricName</span></span>
<span data-ttu-id="26597-116">A szövet neve.</span><span class="sxs-lookup"><span data-stu-id="26597-116">Fabric name.</span></span>

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

### <span data-ttu-id="26597-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="26597-117">-ProviderName</span></span>
<span data-ttu-id="26597-118">Helyreállítási szolgáltató neve</span><span class="sxs-lookup"><span data-stu-id="26597-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="26597-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26597-119">-ResourceGroupName</span></span>
<span data-ttu-id="26597-120">Annak az erőforráscsoportnek a neve, amelyben a helyreállítási szolgáltatások boltozata található.</span><span class="sxs-lookup"><span data-stu-id="26597-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="26597-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="26597-121">-ResourceName</span></span>
<span data-ttu-id="26597-122">A helyreállítási szolgáltatások boltozatának neve.</span><span class="sxs-lookup"><span data-stu-id="26597-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="26597-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="26597-123">-SubscriptionId</span></span>
<span data-ttu-id="26597-124">Az előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="26597-124">The subscription Id.</span></span>

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

### <span data-ttu-id="26597-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26597-125">CommonParameters</span></span>
<span data-ttu-id="26597-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="26597-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26597-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="26597-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26597-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26597-128">INPUTS</span></span>

## <span data-ttu-id="26597-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26597-129">OUTPUTS</span></span>

### <span data-ttu-id="26597-130">Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api20180110. IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="26597-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="26597-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26597-131">NOTES</span></span>

<span data-ttu-id="26597-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="26597-132">ALIASES</span></span>

## <span data-ttu-id="26597-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26597-133">RELATED LINKS</span></span>

