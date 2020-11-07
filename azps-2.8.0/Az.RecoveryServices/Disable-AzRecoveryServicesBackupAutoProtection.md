---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 2613761db4a975f1bd4e04458ccdc5df81c0a2d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838642"
---
# <span data-ttu-id="03eb6-101">Disable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="03eb6-101">Disable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="03eb6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="03eb6-103">Letiltja a védett elemek automatikus biztonsági mentését.</span><span class="sxs-lookup"><span data-stu-id="03eb6-103">Disables auto backup for a protectable item.</span></span>

## <span data-ttu-id="03eb6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03eb6-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03eb6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="03eb6-105">DESCRIPTION</span></span>
<span data-ttu-id="03eb6-106">A **disable-AzRecoveryServicesBackupAutoProtection** parancsmag letiltja a védelmet a védett elemeken.</span><span class="sxs-lookup"><span data-stu-id="03eb6-106">The **Disable-AzRecoveryServicesBackupAutoProtection** cmdlet disables protection on a protectable item.</span></span>

## <span data-ttu-id="03eb6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="03eb6-107">EXAMPLES</span></span>

### <span data-ttu-id="03eb6-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="03eb6-108">Example 1</span></span>
```
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Disable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL"
```

<span data-ttu-id="03eb6-109">Az első parancsmag letiltja a biztonsági mentési házirendet.</span><span class="sxs-lookup"><span data-stu-id="03eb6-109">The first cmdlet disables the Backup protection policy.</span></span>

## <span data-ttu-id="03eb6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03eb6-110">PARAMETERS</span></span>

### <span data-ttu-id="03eb6-111">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="03eb6-111">-BackupManagementType</span></span>
<span data-ttu-id="03eb6-112">Az erőforrás biztonságimásolat-kezelési típusa (például: Mohácsi, DPM).</span><span class="sxs-lookup"><span data-stu-id="03eb6-112">Backup Management type of the resource (for example: MAB, DPM).</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03eb6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03eb6-113">-DefaultProfile</span></span>
<span data-ttu-id="03eb6-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03eb6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03eb6-115">-InputItem</span><span class="sxs-lookup"><span data-stu-id="03eb6-115">-InputItem</span></span>
<span data-ttu-id="03eb6-116">Elem azonosítója</span><span class="sxs-lookup"><span data-stu-id="03eb6-116">Item Id</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03eb6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03eb6-117">-PassThru</span></span>
<span data-ttu-id="03eb6-118">Az automatikus védelem eredményének visszaadása.</span><span class="sxs-lookup"><span data-stu-id="03eb6-118">Return the result for auto protection.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03eb6-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="03eb6-119">-VaultId</span></span>
<span data-ttu-id="03eb6-120">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="03eb6-120">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03eb6-121">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="03eb6-121">-WorkloadType</span></span>
<span data-ttu-id="03eb6-122">Az erőforrás terhelési típusa (például: AzureVM, WindowsServer, AzureFiles).</span><span class="sxs-lookup"><span data-stu-id="03eb6-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles).</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03eb6-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="03eb6-123">-Confirm</span></span>
<span data-ttu-id="03eb6-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="03eb6-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03eb6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03eb6-125">-WhatIf</span></span>
<span data-ttu-id="03eb6-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="03eb6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03eb6-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03eb6-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03eb6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03eb6-128">CommonParameters</span></span>
<span data-ttu-id="03eb6-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03eb6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="03eb6-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03eb6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03eb6-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03eb6-131">INPUTS</span></span>

### <span data-ttu-id="03eb6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="03eb6-132">System.String</span></span>

## <span data-ttu-id="03eb6-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03eb6-133">OUTPUTS</span></span>

### <span data-ttu-id="03eb6-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="03eb6-134">System.Boolean</span></span>

## <span data-ttu-id="03eb6-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03eb6-135">NOTES</span></span>

## <span data-ttu-id="03eb6-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03eb6-136">RELATED LINKS</span></span>
