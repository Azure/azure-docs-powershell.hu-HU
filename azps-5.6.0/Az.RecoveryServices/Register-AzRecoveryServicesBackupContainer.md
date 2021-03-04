---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 83a0e4edd82bd77358df1d95b53e388bb35a9e9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919265"
---
# <span data-ttu-id="04b4f-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="04b4f-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="04b4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04b4f-102">SYNOPSIS</span></span>
<span data-ttu-id="04b4f-103">A **Register-AzRecoveryServicesBackupContainer** parancsmag regisztrál egy Azure VM-et az AzureWorkloadshoz adott workloadType típussal.</span><span class="sxs-lookup"><span data-stu-id="04b4f-103">The **Register-AzRecoveryServicesBackupContainer** cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="04b4f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="04b4f-104">SYNTAX</span></span>

### <span data-ttu-id="04b4f-105">Regisztrálás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="04b4f-105">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04b4f-106">ReRegister</span><span class="sxs-lookup"><span data-stu-id="04b4f-106">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04b4f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="04b4f-107">DESCRIPTION</span></span>
<span data-ttu-id="04b4f-108">Ez a parancs lehetővé teszi, hogy az Azure Biztonsági másolat konvertálja az erőforrást egy biztonságimásolat-tárolóvá, amely ezután regisztrálva lesz a helyreállítási szolgáltatások adott tárolóban.</span><span class="sxs-lookup"><span data-stu-id="04b4f-108">This command allows Azure Backup to convert the Resource to a Backup Container which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="04b4f-109">Az Azure biztonsági mentési szolgáltatás ezután felderítheti az adott munkaterhelés-típus terhelését a tárolón belül, hogy később védve legyen.</span><span class="sxs-lookup"><span data-stu-id="04b4f-109">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="04b4f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="04b4f-110">EXAMPLES</span></span>

### <span data-ttu-id="04b4f-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="04b4f-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="04b4f-112">A parancsmag regisztrál egy azure VM-et az MSSQL-terhelés tárolójaként.</span><span class="sxs-lookup"><span data-stu-id="04b4f-112">The cmdlet registers an azure VM as a container for the workload MSSQL.</span></span>

## <span data-ttu-id="04b4f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04b4f-113">PARAMETERS</span></span>

### <span data-ttu-id="04b4f-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="04b4f-114">-BackupManagementType</span></span>
<span data-ttu-id="04b4f-115">A védett erőforrások osztálya.</span><span class="sxs-lookup"><span data-stu-id="04b4f-115">The class of resources being protected.</span></span> <span data-ttu-id="04b4f-116">A parancsmag által támogatott érték jelenleg az AzureWorkload.</span><span class="sxs-lookup"><span data-stu-id="04b4f-116">Currently the value supported for this cmdlet is AzureWorkload</span></span>

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

### <span data-ttu-id="04b4f-117">-Container</span><span class="sxs-lookup"><span data-stu-id="04b4f-117">-Container</span></span>
<span data-ttu-id="04b4f-118">Tároló, amelyben az elem található</span><span class="sxs-lookup"><span data-stu-id="04b4f-118">Container where the item resides</span></span>

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

### <span data-ttu-id="04b4f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04b4f-119">-DefaultProfile</span></span>
<span data-ttu-id="04b4f-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04b4f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04b4f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="04b4f-121">-Force</span></span>
<span data-ttu-id="04b4f-122">Kényszerítheti a tároló regisztrálását (megakadályozza a megerősítést kérő párbeszédpanelt).</span><span class="sxs-lookup"><span data-stu-id="04b4f-122">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="04b4f-123">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="04b4f-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="04b4f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04b4f-124">-ResourceId</span></span>
<span data-ttu-id="04b4f-125">Annak az Azure-erőforrásnak az azonosítója, amelynek a képviselőjét ellenőrizni kell, ha azt már védi az előfizetésben néhány RecoveryServices-tároló.</span><span class="sxs-lookup"><span data-stu-id="04b4f-125">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="04b4f-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="04b4f-126">-VaultId</span></span>
<span data-ttu-id="04b4f-127">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="04b4f-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="04b4f-128">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="04b4f-128">-WorkloadType</span></span>
<span data-ttu-id="04b4f-129">Az erőforrás terheléstípusa.</span><span class="sxs-lookup"><span data-stu-id="04b4f-129">Workload type of the resource.</span></span> <span data-ttu-id="04b4f-130">A jelenlegi támogatott érték az AzureVM, a WindowsServer, az AzureFiles, az MSSQL</span><span class="sxs-lookup"><span data-stu-id="04b4f-130">The current supported value is AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="04b4f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04b4f-131">-Confirm</span></span>
<span data-ttu-id="04b4f-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="04b4f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04b4f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04b4f-133">-WhatIf</span></span>
<span data-ttu-id="04b4f-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="04b4f-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="04b4f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04b4f-135">CommonParameters</span></span>
<span data-ttu-id="04b4f-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04b4f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04b4f-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04b4f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04b4f-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04b4f-138">INPUTS</span></span>

### <span data-ttu-id="04b4f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="04b4f-139">System.String</span></span>

## <span data-ttu-id="04b4f-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04b4f-140">OUTPUTS</span></span>

### <span data-ttu-id="04b4f-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="04b4f-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="04b4f-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="04b4f-142">NOTES</span></span>

## <span data-ttu-id="04b4f-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04b4f-143">RELATED LINKS</span></span>
