---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 03e990f36c8846ad1055d5d2f8873ead18536128
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838583"
---
# <span data-ttu-id="1e731-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="1e731-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="1e731-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e731-102">SYNOPSIS</span></span>
<span data-ttu-id="1e731-103">Ez a parancs egy bizonyos tárolón vagy az összes regisztrált tárolón belül minden védelemmel ellátott elemet visszakeres.</span><span class="sxs-lookup"><span data-stu-id="1e731-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="1e731-104">A program az alkalmazás hierarchiájának minden elemét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="1e731-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="1e731-105">A DBs és a felsőbb szintű, például a AvailabilityGroup stb.</span><span class="sxs-lookup"><span data-stu-id="1e731-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="1e731-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e731-106">SYNTAX</span></span>

### <span data-ttu-id="1e731-107">NoFilterParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1e731-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e731-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="1e731-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e731-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="1e731-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1e731-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e731-110">DESCRIPTION</span></span>
<span data-ttu-id="1e731-111">A **Get-AzRecoveryServicesBackupProtectableItem** parancsmag a védett elemeket egy tárolóban vagy az Azure biztonsági másolatban szereplő értékkel kapja meg, valamint az elemek védelmi állapotát.</span><span class="sxs-lookup"><span data-stu-id="1e731-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the protectable items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="1e731-112">Az Azure Recovery Services-tárolók számára regisztrált tárolók tartalmazhatnak egy vagy több olyan elemet, amely védett lehet.</span><span class="sxs-lookup"><span data-stu-id="1e731-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="1e731-113">Példák</span><span class="sxs-lookup"><span data-stu-id="1e731-113">EXAMPLES</span></span>

### <span data-ttu-id="1e731-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1e731-114">Example 1</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType MSSQL -Status Registered
PS C:\> $Item = Get-AzRecoveryServicesProtectableItem -Container $Container -ItemType "SQLDatabase" -VaultId $vault.ID
```

<span data-ttu-id="1e731-115">Az első parancs az MSSQL típusú dobozt kapja, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1e731-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="1e731-116">A második parancs beolvassa a biztonsági másolatot a $Container, majd a $Item változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1e731-116">The second command gets the Backup item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="1e731-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e731-117">PARAMETERS</span></span>

### <span data-ttu-id="1e731-118">-Container</span><span class="sxs-lookup"><span data-stu-id="1e731-118">-Container</span></span>
<span data-ttu-id="1e731-119">Tároló, ahol az elem található</span><span class="sxs-lookup"><span data-stu-id="1e731-119">Container where the item resides</span></span>

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

### <span data-ttu-id="1e731-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e731-120">-DefaultProfile</span></span>
<span data-ttu-id="1e731-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e731-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e731-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="1e731-122">-ItemType</span></span>
<span data-ttu-id="1e731-123">A védelemmel ellátott elem típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e731-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="1e731-124">Alkalmazható értékek: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span><span class="sxs-lookup"><span data-stu-id="1e731-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

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

### <span data-ttu-id="1e731-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1e731-125">-Name</span></span>
<span data-ttu-id="1e731-126">Az adatbázis, példány vagy AvailabilityGroup nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e731-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

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

### <span data-ttu-id="1e731-127">-ParentID</span><span class="sxs-lookup"><span data-stu-id="1e731-127">-ParentID</span></span>
<span data-ttu-id="1e731-128">Egy példány vagy AG ÁGÁNAK AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e731-128">Specified the ARM ID of an Instance or AG.</span></span>

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

### <span data-ttu-id="1e731-129">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="1e731-129">-ServerName</span></span>
<span data-ttu-id="1e731-130">Annak a kiszolgálónak a neve, amelyhez az elem tartozik.</span><span class="sxs-lookup"><span data-stu-id="1e731-130">Specifies the name of the server to which the item belongs.</span></span>

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

### <span data-ttu-id="1e731-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="1e731-131">-VaultId</span></span>
<span data-ttu-id="1e731-132">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="1e731-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="1e731-133">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="1e731-133">-WorkloadType</span></span>
<span data-ttu-id="1e731-134">Az erőforrás terhelési típusa (például: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="1e731-134">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

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

### <span data-ttu-id="1e731-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e731-135">CommonParameters</span></span>
<span data-ttu-id="1e731-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e731-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e731-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e731-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e731-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e731-138">INPUTS</span></span>

### <span data-ttu-id="1e731-139">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="1e731-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="1e731-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1e731-140">System.String</span></span>

## <span data-ttu-id="1e731-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e731-141">OUTPUTS</span></span>

### <span data-ttu-id="1e731-142">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ProtectableItemBase</span><span class="sxs-lookup"><span data-stu-id="1e731-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="1e731-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e731-143">NOTES</span></span>

## <span data-ttu-id="1e731-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e731-144">RELATED LINKS</span></span>