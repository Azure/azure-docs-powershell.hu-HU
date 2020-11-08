---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: cfa8abf93fcb7eb4cd3848b1a5f69cf28a5fe6ab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184251"
---
# <span data-ttu-id="c8413-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="c8413-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="c8413-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8413-102">SYNOPSIS</span></span>
<span data-ttu-id="c8413-103">A **Register-AzRecoveryServicesBackupContainer** parancsmag egy Azure VM-et rögzít az AzureWorkloads meghatározott workloadType.</span><span class="sxs-lookup"><span data-stu-id="c8413-103">The **Register-AzRecoveryServicesBackupContainer** cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="c8413-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8413-104">SYNTAX</span></span>

### <span data-ttu-id="c8413-105">Register (default)</span><span class="sxs-lookup"><span data-stu-id="c8413-105">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8413-106">Újraregisztrálása</span><span class="sxs-lookup"><span data-stu-id="c8413-106">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8413-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8413-107">DESCRIPTION</span></span>
<span data-ttu-id="c8413-108">Ez a parancs lehetővé teszi az Azure Backup-nek, hogy az erőforrást egy olyan biztonsági tárolóba konvertálja, amelyet azután regisztráltak az adott helyreállítási szolgáltatások boltozata számára.</span><span class="sxs-lookup"><span data-stu-id="c8413-108">This command allows Azure Backup to convert the Resource to a Backup Container which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="c8413-109">Az Azure Backup szolgáltatással később is megtudhatja, hogy az adott terhelési típus munkafolyamata később védett legyen.</span><span class="sxs-lookup"><span data-stu-id="c8413-109">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="c8413-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c8413-110">EXAMPLES</span></span>

### <span data-ttu-id="c8413-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c8413-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="c8413-112">A parancsmag egy Azure VM tárolót rögzít az MSSQL-munkaterheléshez.</span><span class="sxs-lookup"><span data-stu-id="c8413-112">The cmdlet registers an azure VM as a container for the workload MSSQL.</span></span>

## <span data-ttu-id="c8413-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8413-113">PARAMETERS</span></span>

### <span data-ttu-id="c8413-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="c8413-114">-BackupManagementType</span></span>
<span data-ttu-id="c8413-115">A védelemmel ellátott erőforrások osztálya.</span><span class="sxs-lookup"><span data-stu-id="c8413-115">The class of resources being protected.</span></span> <span data-ttu-id="c8413-116">A parancsmag által támogatott érték jelenleg a AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="c8413-116">Currently the value supported for this cmdlet is AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8413-117">-Container</span><span class="sxs-lookup"><span data-stu-id="c8413-117">-Container</span></span>
<span data-ttu-id="c8413-118">Tároló, ahol az elem található</span><span class="sxs-lookup"><span data-stu-id="c8413-118">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: ReRegister
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8413-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8413-119">-DefaultProfile</span></span>
<span data-ttu-id="c8413-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8413-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8413-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c8413-121">-Force</span></span>
<span data-ttu-id="c8413-122">A regiszterek nyilvántartása tároló (megakadályozza a megerősítést kérő párbeszédpanelt).</span><span class="sxs-lookup"><span data-stu-id="c8413-122">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="c8413-123">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="c8413-123">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8413-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8413-124">-ResourceId</span></span>
<span data-ttu-id="c8413-125">Annak az Azure-erőforrásnak az AZONOSÍTÓját, amelynek a reprezentatív elemét ellenőrizni kell, ha az előfizetésben egy RecoveryServices-tároló már védett.</span><span class="sxs-lookup"><span data-stu-id="c8413-125">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Register
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8413-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="c8413-126">-VaultId</span></span>
<span data-ttu-id="c8413-127">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="c8413-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c8413-128">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="c8413-128">-WorkloadType</span></span>
<span data-ttu-id="c8413-129">Az erőforrás terhelési típusa.</span><span class="sxs-lookup"><span data-stu-id="c8413-129">Workload type of the resource.</span></span> <span data-ttu-id="c8413-130">Az aktuálisan támogatott érték a AzureVM, az WindowsServer, az AzureFiles, az MSSQL</span><span class="sxs-lookup"><span data-stu-id="c8413-130">The current supported value is AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8413-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c8413-131">-Confirm</span></span>
<span data-ttu-id="c8413-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c8413-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8413-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8413-133">-WhatIf</span></span>
<span data-ttu-id="c8413-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c8413-134">Shows what would happen if the cmdlet runs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8413-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8413-135">CommonParameters</span></span>
<span data-ttu-id="c8413-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8413-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8413-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c8413-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8413-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8413-138">INPUTS</span></span>

### <span data-ttu-id="c8413-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c8413-139">System.String</span></span>

## <span data-ttu-id="c8413-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8413-140">OUTPUTS</span></span>

### <span data-ttu-id="c8413-141">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="c8413-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="c8413-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8413-142">NOTES</span></span>

## <span data-ttu-id="c8413-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8413-143">RELATED LINKS</span></span>
