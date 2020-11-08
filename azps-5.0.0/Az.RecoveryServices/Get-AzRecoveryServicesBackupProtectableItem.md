---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: add399ca208cdcd1f1b4395523f8df43875ff451
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194194"
---
# <span data-ttu-id="52aa0-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="52aa0-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="52aa0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="52aa0-102">SYNOPSIS</span></span>
<span data-ttu-id="52aa0-103">Ez a parancs egy bizonyos tárolón vagy az összes regisztrált tárolón belül minden védelemmel ellátott elemet visszakeres.</span><span class="sxs-lookup"><span data-stu-id="52aa0-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="52aa0-104">A program az alkalmazás hierarchiájának minden elemét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="52aa0-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="52aa0-105">A DBs és a felsőbb szintű, például a AvailabilityGroup stb.</span><span class="sxs-lookup"><span data-stu-id="52aa0-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="52aa0-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="52aa0-106">SYNTAX</span></span>

### <span data-ttu-id="52aa0-107">NoFilterParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="52aa0-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52aa0-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="52aa0-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52aa0-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="52aa0-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52aa0-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="52aa0-110">DESCRIPTION</span></span>
<span data-ttu-id="52aa0-111">A **Get-AzRecoveryServicesBackupProtectableItem** parancsmag a védett elemek listáját a tárolóban és az elemek védelmi állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="52aa0-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the list of protectable items in a container and the protection status of the items.</span></span>
<span data-ttu-id="52aa0-112">Az Azure Recovery Services-tárolók számára regisztrált tárolók tartalmazhatnak egy vagy több olyan elemet, amely védett lehet.</span><span class="sxs-lookup"><span data-stu-id="52aa0-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="52aa0-113">Példák</span><span class="sxs-lookup"><span data-stu-id="52aa0-113">EXAMPLES</span></span>

### <span data-ttu-id="52aa0-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="52aa0-114">Example 1</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType MSSQL -Status Registered
PS C:\> $Item = Get-AzRecoveryServicesProtectableItem -Container $Container -ItemType "SQLDatabase" -VaultId $vault.ID
```

<span data-ttu-id="52aa0-115">Az első parancs az MSSQL típusú dobozt kapja, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="52aa0-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="52aa0-116">A második parancs beolvassa a biztonsági mentésre szolgáló elemet $Container, majd a $Item változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="52aa0-116">The second command gets the Backup protectable item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="52aa0-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="52aa0-117">PARAMETERS</span></span>

### <span data-ttu-id="52aa0-118">-Container</span><span class="sxs-lookup"><span data-stu-id="52aa0-118">-Container</span></span>
<span data-ttu-id="52aa0-119">Tároló, ahol az elem található</span><span class="sxs-lookup"><span data-stu-id="52aa0-119">Container where the item resides</span></span>

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

### <span data-ttu-id="52aa0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52aa0-120">-DefaultProfile</span></span>
<span data-ttu-id="52aa0-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="52aa0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52aa0-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="52aa0-122">-ItemType</span></span>
<span data-ttu-id="52aa0-123">A védelemmel ellátott elem típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="52aa0-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="52aa0-124">Alkalmazható értékek: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span><span class="sxs-lookup"><span data-stu-id="52aa0-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

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

### <span data-ttu-id="52aa0-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="52aa0-125">-Name</span></span>
<span data-ttu-id="52aa0-126">Az adatbázis, példány vagy AvailabilityGroup nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="52aa0-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

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

### <span data-ttu-id="52aa0-127">-ParentID</span><span class="sxs-lookup"><span data-stu-id="52aa0-127">-ParentID</span></span>
<span data-ttu-id="52aa0-128">Egy példány vagy AG ÁGÁNAK AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="52aa0-128">Specified the ARM ID of an Instance or AG.</span></span>

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

### <span data-ttu-id="52aa0-129">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="52aa0-129">-ServerName</span></span>
<span data-ttu-id="52aa0-130">Annak a kiszolgálónak a neve, amelyhez az elem tartozik.</span><span class="sxs-lookup"><span data-stu-id="52aa0-130">Specifies the name of the server to which the item belongs.</span></span>

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

### <span data-ttu-id="52aa0-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="52aa0-131">-VaultId</span></span>
<span data-ttu-id="52aa0-132">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="52aa0-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="52aa0-133">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="52aa0-133">-WorkloadType</span></span>
<span data-ttu-id="52aa0-134">Az erőforrás terhelési típusa.</span><span class="sxs-lookup"><span data-stu-id="52aa0-134">Workload type of the resource.</span></span> <span data-ttu-id="52aa0-135">Az aktuálisan támogatott értékek a AzureVM, az WindowsServer, az AzureFiles, az MSSQL</span><span class="sxs-lookup"><span data-stu-id="52aa0-135">The current supported values are  AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:
Accepted values: AzureVM, WindowsServer, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52aa0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52aa0-136">CommonParameters</span></span>
<span data-ttu-id="52aa0-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="52aa0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52aa0-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="52aa0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52aa0-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="52aa0-139">INPUTS</span></span>

### <span data-ttu-id="52aa0-140">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="52aa0-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="52aa0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="52aa0-141">System.String</span></span>

## <span data-ttu-id="52aa0-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52aa0-142">OUTPUTS</span></span>

### <span data-ttu-id="52aa0-143">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ProtectableItemBase</span><span class="sxs-lookup"><span data-stu-id="52aa0-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="52aa0-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="52aa0-144">NOTES</span></span>

## <span data-ttu-id="52aa0-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52aa0-145">RELATED LINKS</span></span>
