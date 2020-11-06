---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 856B76FC-88ED-4A29-9DC6-C482398D702E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
ms.openlocfilehash: b449b96417f0ac05fa857a48a10143a285ed888f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493857"
---
# <span data-ttu-id="f6856-101">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="f6856-101">Restore-AzureRmBackupItem</span></span>

## <span data-ttu-id="f6856-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6856-102">SYNOPSIS</span></span>
<span data-ttu-id="f6856-103">Egy biztonsági elem adatainak és konfigurációjának visszaállítása a helyreállítási pontra.</span><span class="sxs-lookup"><span data-stu-id="f6856-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6856-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6856-104">SYNTAX</span></span>

```
Restore-AzureRmBackupItem [-StorageAccountName] <String> [-RecoveryPoint] <AzureRMBackupRecoveryPoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6856-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6856-105">DESCRIPTION</span></span>
<span data-ttu-id="f6856-106">A **Restore-AzureRmBackupItem** parancsmag visszaállítja az Azure Backup-elemek adatát és konfigurációját egy megadott helyreállítási pontra.</span><span class="sxs-lookup"><span data-stu-id="f6856-106">The **Restore-AzureRmBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="f6856-107">Ez a parancsmag a biztonságimásolat-tárolóból a fiókba való visszaállítást indítja el.</span><span class="sxs-lookup"><span data-stu-id="f6856-107">This cmdlet starts the restore from the Backup vault to your account.</span></span>

<span data-ttu-id="f6856-108">A visszaállítási művelet nem állítja vissza a teljes virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="f6856-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="f6856-109">Visszaállítja a lemez adatait és a konfigurációs információkat.</span><span class="sxs-lookup"><span data-stu-id="f6856-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="f6856-110">A visszaállítási művelet befejezése után létre kell hoznia a virtuális gépet, és el kell indítania.</span><span class="sxs-lookup"><span data-stu-id="f6856-110">After the restore operation finished, you must create the virtual machine and start it.</span></span>

## <span data-ttu-id="f6856-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f6856-111">EXAMPLES</span></span>

### <span data-ttu-id="f6856-112">Példa 1: virtuális gép visszaállítása helyreállítási pontra</span><span class="sxs-lookup"><span data-stu-id="f6856-112">Example 1: Restore a virtual machine to a recovery point</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> $RecoveryPoint = Get-AzureRmBackupRecoveryPoint -Item $BackupItem 
PS C:\> Restore-AzureRmBackupItem -StorageAccountName "DestinationAccount" -RecoveryPoint $RecoveryPoint 
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Restore         InProgress      26-Aug-15 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="f6856-113">Az első parancs a Vault03 nevű boltozatot az Get-AzureRmBackupVault parancsmag segítségével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f6856-113">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="f6856-114">A parancs az objektumot a $Vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f6856-114">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="f6856-115">A második parancs a **Get-AzureRmBackupContainer** parancsmaggal egy olyan tárolót kap, amelyben a megadott név szerepel a boltozaton $Vault.</span><span class="sxs-lookup"><span data-stu-id="f6856-115">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="f6856-116">A parancs az objektumot a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f6856-116">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="f6856-117">A harmadik parancs a **Get-AzureRmBackupItem** parancsmag használatával kapja meg a biztonsági másolatot a $Container tárolójában.</span><span class="sxs-lookup"><span data-stu-id="f6856-117">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="f6856-118">A parancs az objektumot a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f6856-118">The command stores that object in the $BackupItem variable.</span></span>

<span data-ttu-id="f6856-119">A negyedik parancs a $BackupItemben található elem helyreállítási pontját kapja.</span><span class="sxs-lookup"><span data-stu-id="f6856-119">The fourth command gets recovery point for the item in $BackupItem.</span></span>
<span data-ttu-id="f6856-120">A parancs az objektumot a $RecoveryPoint változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f6856-120">The command stores that object in the $RecoveryPoint variable.</span></span>

<span data-ttu-id="f6856-121">A végleges parancs visszaállítja a $RecoveryPoint helyreállítási pontját a DestinationAccount nevű fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="f6856-121">The final command restores the recovery point in $RecoveryPoint for the account named DestinationAccount.</span></span>

## <span data-ttu-id="f6856-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6856-122">PARAMETERS</span></span>

### <span data-ttu-id="f6856-123">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f6856-123">-RecoveryPoint</span></span>
<span data-ttu-id="f6856-124">Annak a helyreállítási pontnak a meghatározása, amelyre a virtuális gépet vissza szeretné állítani.</span><span class="sxs-lookup"><span data-stu-id="f6856-124">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="f6856-125">Ha **AzureRmBackupRecoveryPoint** szeretne beolvasni, használja az Get-AzureRmBackupRecoveryPoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f6856-125">To obtain an **AzureRmBackupRecoveryPoint** , use the Get-AzureRmBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6856-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f6856-126">-StorageAccountName</span></span>
<span data-ttu-id="f6856-127">Az előfizetésben a TARGET Storage fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6856-127">Specifies the name of the target storage account in your subscription.</span></span>
<span data-ttu-id="f6856-128">A visszaállítási folyamat részeként ez a parancsmag tárolja a lemezeket és a konfigurációs információkat ebben a tárolási fiókban.</span><span class="sxs-lookup"><span data-stu-id="f6856-128">As a part of the restore process, this cmdlet stores the disks and the configuration information in this storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6856-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6856-129">-DefaultProfile</span></span>
<span data-ttu-id="f6856-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6856-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6856-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6856-131">CommonParameters</span></span>
<span data-ttu-id="f6856-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6856-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6856-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6856-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6856-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6856-134">INPUTS</span></span>

### <span data-ttu-id="f6856-135">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f6856-135">AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="f6856-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6856-136">OUTPUTS</span></span>

### <span data-ttu-id="f6856-137">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="f6856-137">AzureRmBackupJob</span></span>

## <span data-ttu-id="f6856-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6856-138">NOTES</span></span>

## <span data-ttu-id="f6856-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6856-139">RELATED LINKS</span></span>

[<span data-ttu-id="f6856-140">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="f6856-140">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="f6856-141">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="f6856-141">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="f6856-142">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f6856-142">Get-AzureRmBackupRecoveryPoint</span></span>](./Get-AzureRmBackupRecoveryPoint.md)


