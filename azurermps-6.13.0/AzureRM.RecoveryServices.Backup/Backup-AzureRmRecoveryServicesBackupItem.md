---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/backup-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 9838db99fa1126f3948bb16f9ee16180cb652904
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494971"
---
# <span data-ttu-id="8e344-101">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8e344-101">Backup-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="8e344-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e344-102">SYNOPSIS</span></span>
<span data-ttu-id="8e344-103">Biztonságimásolat-elem biztonsági másolatának indítása</span><span class="sxs-lookup"><span data-stu-id="8e344-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e344-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e344-104">SYNTAX</span></span>

```
Backup-AzureRmRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e344-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e344-105">DESCRIPTION</span></span>
<span data-ttu-id="8e344-106">A **Backup-AzureRmRecoveryServicesBackupItem** parancsmag egy olyan védett Azure biztonsági másolat biztonsági másolatát indítja el, amely nincs a biztonsági ütemtervhez kötve.</span><span class="sxs-lookup"><span data-stu-id="8e344-106">The **Backup-AzureRmRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="8e344-107">A kezdeti biztonsági mentés után azonnal elvégezheti a biztonsági mentést, ha az ütemezett biztonsági mentés után nem tud biztonsági másolatot indítani.</span><span class="sxs-lookup"><span data-stu-id="8e344-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="8e344-108">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="8e344-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="8e344-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8e344-109">EXAMPLES</span></span>

### <span data-ttu-id="8e344-110">1. példa: biztonsági másolat készítése biztonsági elemről</span><span class="sxs-lookup"><span data-stu-id="8e344-110">Example 1: Start a backup for a Backup item</span></span>
```
PS C:\> $NamedContainer = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "pstestv2vm1" 
PS C:\> $Item = Get-AzureRmRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM 
PS C:\> $Job = Backup-AzureRmRecoveryServicesItem -Item $Item
Operation        Status               StartTime            EndTime                   JOBID                           
------------     ---------            ------               ---------                 -------                                         
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="8e344-111">Az első parancs a AzureVM nevű pstestv2vm1 nevű tartalék tárolót kapja, majd a $NamedContainer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8e344-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="8e344-112">A második parancs a $NamedContainer tárolóhoz tartozó biztonsági másolatot kapja, majd a $Item változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8e344-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="8e344-113">Az utolsó parancs elindítja a biztonsági mentési feladatot a $Itemban.</span><span class="sxs-lookup"><span data-stu-id="8e344-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="8e344-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e344-114">PARAMETERS</span></span>

### <span data-ttu-id="8e344-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e344-115">-DefaultProfile</span></span>
<span data-ttu-id="8e344-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e344-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e344-117">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="8e344-117">-ExpiryDateTimeUTC</span></span>
<span data-ttu-id="8e344-118">A lejárat időpontját **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e344-118">Specifies an expiry time as a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e344-119">-Elem</span><span class="sxs-lookup"><span data-stu-id="8e344-119">-Item</span></span>
<span data-ttu-id="8e344-120">Annak a biztonságimásolat-elemnek a megadása, amelyhez ez a parancsmag elindítja a biztonsági mentési műveletet.</span><span class="sxs-lookup"><span data-stu-id="8e344-120">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e344-121">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8e344-121">-VaultId</span></span>
<span data-ttu-id="8e344-122">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="8e344-122">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8e344-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8e344-123">-Confirm</span></span>
<span data-ttu-id="8e344-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8e344-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e344-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e344-125">-WhatIf</span></span>
<span data-ttu-id="8e344-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8e344-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e344-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e344-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e344-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e344-128">CommonParameters</span></span>
<span data-ttu-id="8e344-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e344-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e344-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e344-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e344-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e344-131">INPUTS</span></span>

### <span data-ttu-id="8e344-132">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="8e344-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="8e344-133">Paraméterek: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8e344-133">Parameters: Item (ByValue)</span></span>

### <span data-ttu-id="8e344-134">System. null ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8e344-134">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="8e344-135">System. String</span><span class="sxs-lookup"><span data-stu-id="8e344-135">System.String</span></span>
<span data-ttu-id="8e344-136">Paraméterek: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8e344-136">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="8e344-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e344-137">OUTPUTS</span></span>

### <span data-ttu-id="8e344-138">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="8e344-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="8e344-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e344-139">NOTES</span></span>

## <span data-ttu-id="8e344-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e344-140">RELATED LINKS</span></span>

[<span data-ttu-id="8e344-141">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="8e344-141">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="8e344-142">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8e344-142">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="8e344-143">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8e344-143">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


