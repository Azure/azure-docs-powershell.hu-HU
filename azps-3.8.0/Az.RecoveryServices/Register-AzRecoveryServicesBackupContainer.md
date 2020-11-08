---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: a6c47561b8fdb9e748940c917d85548d25be1ccf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012682"
---
# <span data-ttu-id="a859d-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="a859d-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="a859d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a859d-102">SYNOPSIS</span></span>
<span data-ttu-id="a859d-103">Ez a parancs lehetővé teszi az Azure Backup-nek, hogy az erőforrást egy olyan biztonsági tárolóba konvertálja, amelyet azután regisztráltak az adott helyreállítási szolgáltatások boltozata számára.</span><span class="sxs-lookup"><span data-stu-id="a859d-103">This command allows Azure Backup to convert the �Resource� to a �Backup Container� which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="a859d-104">Az Azure Backup szolgáltatással később is megtudhatja, hogy az adott terhelési típus munkafolyamata később védett legyen.</span><span class="sxs-lookup"><span data-stu-id="a859d-104">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="a859d-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a859d-105">SYNTAX</span></span>

### <span data-ttu-id="a859d-106">Register (default)</span><span class="sxs-lookup"><span data-stu-id="a859d-106">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a859d-107">Újraregisztrálása</span><span class="sxs-lookup"><span data-stu-id="a859d-107">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a859d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a859d-108">DESCRIPTION</span></span>
<span data-ttu-id="a859d-109">A parancsmag egy Azure VM-et regisztrál a AzureWorkloads meghatározott workloadType.</span><span class="sxs-lookup"><span data-stu-id="a859d-109">The cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="a859d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a859d-110">EXAMPLES</span></span>

### <span data-ttu-id="a859d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a859d-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="a859d-112">A parancsmag egy Azure VM-munkaterhelést rögzít az MSSQL-nek.</span><span class="sxs-lookup"><span data-stu-id="a859d-112">The cmdlet registers an azure VM for the workload MSSQL.</span></span>

## <span data-ttu-id="a859d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a859d-113">PARAMETERS</span></span>

### <span data-ttu-id="a859d-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="a859d-114">-BackupManagementType</span></span>
<span data-ttu-id="a859d-115">Az Azure Backup tároló biztonsági másolatának típusa</span><span class="sxs-lookup"><span data-stu-id="a859d-115">The backup management type of the Azure Backup container</span></span>

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

### <span data-ttu-id="a859d-116">-Container</span><span class="sxs-lookup"><span data-stu-id="a859d-116">-Container</span></span>
<span data-ttu-id="a859d-117">Tároló, ahol az elem található</span><span class="sxs-lookup"><span data-stu-id="a859d-117">Container where the item resides</span></span>

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

### <span data-ttu-id="a859d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a859d-118">-DefaultProfile</span></span>
<span data-ttu-id="a859d-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a859d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a859d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a859d-120">-Force</span></span>
<span data-ttu-id="a859d-121">A regiszterek nyilvántartása tároló (megakadályozza a megerősítést kérő párbeszédpanelt).</span><span class="sxs-lookup"><span data-stu-id="a859d-121">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="a859d-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="a859d-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="a859d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a859d-123">-ResourceId</span></span>
<span data-ttu-id="a859d-124">Annak az Azure-erőforrásnak az AZONOSÍTÓját, amelynek a reprezentatív elemét ellenőrizni kell, ha az előfizetésben egy RecoveryServices-tároló már védett.</span><span class="sxs-lookup"><span data-stu-id="a859d-124">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="a859d-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a859d-125">-VaultId</span></span>
<span data-ttu-id="a859d-126">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="a859d-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a859d-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="a859d-127">-WorkloadType</span></span>
<span data-ttu-id="a859d-128">Az erőforrás terhelési típusa (például: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="a859d-128">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

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

### <span data-ttu-id="a859d-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a859d-129">-Confirm</span></span>
<span data-ttu-id="a859d-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a859d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a859d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a859d-131">-WhatIf</span></span>
<span data-ttu-id="a859d-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a859d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a859d-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a859d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a859d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a859d-134">CommonParameters</span></span>
<span data-ttu-id="a859d-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a859d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a859d-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a859d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a859d-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a859d-137">INPUTS</span></span>

### <span data-ttu-id="a859d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a859d-138">System.String</span></span>

## <span data-ttu-id="a859d-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a859d-139">OUTPUTS</span></span>

### <span data-ttu-id="a859d-140">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="a859d-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="a859d-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a859d-141">NOTES</span></span>

## <span data-ttu-id="a859d-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a859d-142">RELATED LINKS</span></span>
