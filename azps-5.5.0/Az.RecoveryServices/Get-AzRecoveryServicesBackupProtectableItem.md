---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 580f5fd7dc85857bff7257847806bb15dc646ad3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158610"
---
# <span data-ttu-id="b70f6-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="b70f6-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="b70f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b70f6-102">SYNOPSIS</span></span>
<span data-ttu-id="b70f6-103">Ez a parancs beolvassa az összes védett elemet egy adott tárolón belül vagy az összes regisztrált tárolóban.</span><span class="sxs-lookup"><span data-stu-id="b70f6-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="b70f6-104">Az alkalmazás hierarchiájának összes elemét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b70f6-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="b70f6-105">Visszaadja a DBs-eket és azok felsőbb szintű entitását, például a Instance, az AvailabilityGroup stb.</span><span class="sxs-lookup"><span data-stu-id="b70f6-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="b70f6-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b70f6-106">SYNTAX</span></span>

### <span data-ttu-id="b70f6-107">NoFilterParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b70f6-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b70f6-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="b70f6-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b70f6-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="b70f6-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b70f6-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b70f6-110">DESCRIPTION</span></span>
<span data-ttu-id="b70f6-111">A **Get-AzRecoveryServicesBackupProtectableItem** parancsmag lekérte a tárolóban lévő védhető elemek listáját és az elemek védelmi állapotát.</span><span class="sxs-lookup"><span data-stu-id="b70f6-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the list of protectable items in a container and the protection status of the items.</span></span>
<span data-ttu-id="b70f6-112">Az Azure Recovery Services-tárolókban regisztrált tárolókban egy vagy több védett elem is lehet.</span><span class="sxs-lookup"><span data-stu-id="b70f6-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="b70f6-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b70f6-113">EXAMPLES</span></span>

### <span data-ttu-id="b70f6-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="b70f6-114">Example 1</span></span>
```
PS C:\> $Vault = Get-AzRecoveryServicesVault -Name "MyRecoveryVault"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer -Status Registered -VaultId $Vault.Id
PS C:\> $Item = Get-AzRecoveryServicesBackupProtectableItem -Container $Container -ItemType "SQLInstance" -WorkloadType "MSSQL" -VaultId $Vault.ID
```

<span data-ttu-id="b70f6-115">Az első parancs lekérte az MSSQL típusú tárolót, majd a $Container tárolja.</span><span class="sxs-lookup"><span data-stu-id="b70f6-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="b70f6-116">A második parancs a biztonsági másolat védett elemét $Container, majd a $Item tárolja.</span><span class="sxs-lookup"><span data-stu-id="b70f6-116">The second command gets the Backup protectable item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="b70f6-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b70f6-117">PARAMETERS</span></span>

### <span data-ttu-id="b70f6-118">-Container</span><span class="sxs-lookup"><span data-stu-id="b70f6-118">-Container</span></span>
<span data-ttu-id="b70f6-119">Tároló, amelyben az elem található</span><span class="sxs-lookup"><span data-stu-id="b70f6-119">Container where the item resides</span></span>

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

### <span data-ttu-id="b70f6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b70f6-120">-DefaultProfile</span></span>
<span data-ttu-id="b70f6-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b70f6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b70f6-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="b70f6-122">-ItemType</span></span>
<span data-ttu-id="b70f6-123">A védett elem típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b70f6-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="b70f6-124">Alkalmazható értékek: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span><span class="sxs-lookup"><span data-stu-id="b70f6-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

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

### <span data-ttu-id="b70f6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b70f6-125">-Name</span></span>
<span data-ttu-id="b70f6-126">Az adatbázis, a példány vagy az elérhetőségi csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b70f6-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

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

### <span data-ttu-id="b70f6-127">-ParentID</span><span class="sxs-lookup"><span data-stu-id="b70f6-127">-ParentID</span></span>
<span data-ttu-id="b70f6-128">Egy példány ARM AG azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b70f6-128">Specified the ARM ID of an Instance or AG.</span></span>

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

### <span data-ttu-id="b70f6-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b70f6-129">-ServerName</span></span>
<span data-ttu-id="b70f6-130">Annak a kiszolgálónak a nevét adja meg, amelyhez az elem tartozik.</span><span class="sxs-lookup"><span data-stu-id="b70f6-130">Specifies the name of the server to which the item belongs.</span></span>

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

### <span data-ttu-id="b70f6-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b70f6-131">-VaultId</span></span>
<span data-ttu-id="b70f6-132">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b70f6-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b70f6-133">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="b70f6-133">-WorkloadType</span></span>
<span data-ttu-id="b70f6-134">Az erőforrás terheléstípusa.</span><span class="sxs-lookup"><span data-stu-id="b70f6-134">Workload type of the resource.</span></span> <span data-ttu-id="b70f6-135">Az aktuálisan támogatott értékek: AzureVM, WindowsServer, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="b70f6-135">The current supported values are  AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="b70f6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b70f6-136">CommonParameters</span></span>
<span data-ttu-id="b70f6-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b70f6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b70f6-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b70f6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b70f6-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b70f6-139">INPUTS</span></span>

### <span data-ttu-id="b70f6-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="b70f6-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="b70f6-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b70f6-141">System.String</span></span>

## <span data-ttu-id="b70f6-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b70f6-142">OUTPUTS</span></span>

### <span data-ttu-id="b70f6-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span><span class="sxs-lookup"><span data-stu-id="b70f6-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="b70f6-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b70f6-144">NOTES</span></span>

## <span data-ttu-id="b70f6-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b70f6-145">RELATED LINKS</span></span>
