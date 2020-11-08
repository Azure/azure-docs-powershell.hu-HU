---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 293cd11c146369644ca67ba76158c251b1480d22
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014736"
---
# <span data-ttu-id="162c8-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="162c8-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="162c8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="162c8-102">SYNOPSIS</span></span>
<span data-ttu-id="162c8-103">Ez a parancs egy bizonyos tárolón vagy az összes regisztrált tárolón belül minden védelemmel ellátott elemet visszakeres.</span><span class="sxs-lookup"><span data-stu-id="162c8-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="162c8-104">A program az alkalmazás hierarchiájának minden elemét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="162c8-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="162c8-105">A DBs és a felsőbb szintű, például a AvailabilityGroup stb.</span><span class="sxs-lookup"><span data-stu-id="162c8-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="162c8-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="162c8-106">SYNTAX</span></span>

### <span data-ttu-id="162c8-107">NoFilterParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="162c8-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="162c8-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="162c8-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="162c8-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="162c8-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="162c8-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="162c8-110">DESCRIPTION</span></span>
<span data-ttu-id="162c8-111">A **Get-AzRecoveryServicesBackupProtectableItem** parancsmag a védett elemeket egy tárolóban vagy az Azure biztonsági másolatban szereplő értékkel kapja meg, valamint az elemek védelmi állapotát.</span><span class="sxs-lookup"><span data-stu-id="162c8-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the protectable items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="162c8-112">Az Azure Recovery Services-tárolók számára regisztrált tárolók tartalmazhatnak egy vagy több olyan elemet, amely védett lehet.</span><span class="sxs-lookup"><span data-stu-id="162c8-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="162c8-113">Példák</span><span class="sxs-lookup"><span data-stu-id="162c8-113">EXAMPLES</span></span>

### <span data-ttu-id="162c8-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="162c8-114">Example 1</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType MSSQL -Status Registered
PS C:\> $Item = Get-AzRecoveryServicesProtectableItem -Container $Container -ItemType "SQLDatabase" -VaultId $vault.ID
```

<span data-ttu-id="162c8-115">Az első parancs az MSSQL típusú dobozt kapja, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="162c8-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="162c8-116">A második parancs beolvassa a biztonsági másolatot a $Container, majd a $Item változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="162c8-116">The second command gets the Backup item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="162c8-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="162c8-117">PARAMETERS</span></span>

### <span data-ttu-id="162c8-118">-Container</span><span class="sxs-lookup"><span data-stu-id="162c8-118">-Container</span></span>
<span data-ttu-id="162c8-119">Tároló, ahol az elem található</span><span class="sxs-lookup"><span data-stu-id="162c8-119">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="162c8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="162c8-120">-DefaultProfile</span></span>
<span data-ttu-id="162c8-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="162c8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="162c8-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="162c8-122">-ItemType</span></span>
<span data-ttu-id="162c8-123">A védelemmel ellátott elem típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="162c8-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="162c8-124">Alkalmazható értékek: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span><span class="sxs-lookup"><span data-stu-id="162c8-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemType
Parameter Sets: FilterParamSet, IdParamSet
Aliases:
Accepted values: SQLDataBase, SQLInstance, SQLAvailabilityGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="162c8-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="162c8-125">-Name</span></span>
<span data-ttu-id="162c8-126">Az adatbázis, példány vagy AvailabilityGroup nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="162c8-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="162c8-127">-ParentID</span><span class="sxs-lookup"><span data-stu-id="162c8-127">-ParentID</span></span>
<span data-ttu-id="162c8-128">Egy példány vagy AG ÁGÁNAK AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="162c8-128">Specified the ARM ID of an Instance or AG.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="162c8-129">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="162c8-129">-ServerName</span></span>
<span data-ttu-id="162c8-130">Annak a kiszolgálónak a neve, amelyhez az elem tartozik.</span><span class="sxs-lookup"><span data-stu-id="162c8-130">Specifies the name of the server to which the item belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="162c8-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="162c8-131">-VaultId</span></span>
<span data-ttu-id="162c8-132">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="162c8-132">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="162c8-133">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="162c8-133">-WorkloadType</span></span>
<span data-ttu-id="162c8-134">Az erőforrás terhelési típusa (például: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="162c8-134">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="162c8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="162c8-135">CommonParameters</span></span>
<span data-ttu-id="162c8-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="162c8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="162c8-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="162c8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="162c8-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="162c8-138">INPUTS</span></span>

### <span data-ttu-id="162c8-139">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="162c8-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="162c8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="162c8-140">System.String</span></span>

## <span data-ttu-id="162c8-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="162c8-141">OUTPUTS</span></span>

### <span data-ttu-id="162c8-142">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ProtectableItemBase</span><span class="sxs-lookup"><span data-stu-id="162c8-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="162c8-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="162c8-143">NOTES</span></span>

## <span data-ttu-id="162c8-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="162c8-144">RELATED LINKS</span></span>
