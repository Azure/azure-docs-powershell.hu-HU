---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/disable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 7235c70eae1ab7b93340e68bbb705c17b74c3408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493085"
---
# <span data-ttu-id="20967-101">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="20967-101">Disable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="20967-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20967-102">SYNOPSIS</span></span>
<span data-ttu-id="20967-103">Letiltja a biztonsági mentéssel védett elemek védelmét.</span><span class="sxs-lookup"><span data-stu-id="20967-103">Disables protection for a Backup-protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20967-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20967-104">SYNTAX</span></span>

```
Disable-AzureRmRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20967-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="20967-105">DESCRIPTION</span></span>
<span data-ttu-id="20967-106">A **disable-AzureRmRecoveryServicesBackupProtection** parancsmag letiltja az Azure biztonsági másolattal védett elemek védelmét.</span><span class="sxs-lookup"><span data-stu-id="20967-106">The **Disable-AzureRmRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="20967-107">Ez a parancsmag leállítja az elemek rendszeres ütemezett biztonsági mentését.</span><span class="sxs-lookup"><span data-stu-id="20967-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="20967-108">Ez a parancsmag a biztonsági másolat meglévő helyreállítási pontját is törölheti.</span><span class="sxs-lookup"><span data-stu-id="20967-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>

<span data-ttu-id="20967-109">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="20967-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="20967-110">Példák</span><span class="sxs-lookup"><span data-stu-id="20967-110">EXAMPLES</span></span>

### <span data-ttu-id="20967-111">1. példa: biztonsági másolat elleni védelem letiltása</span><span class="sxs-lookup"><span data-stu-id="20967-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzureRmRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzureRmRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="20967-112">Az első parancs a biztonságimásolat-tárolók tömbjét kapja, majd a $Cont tömbben tárolja.</span><span class="sxs-lookup"><span data-stu-id="20967-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>

<span data-ttu-id="20967-113">A második parancs az első tároló elemnek megfelelő biztonsági másolatot kapja, majd a $PI változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="20967-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>

<span data-ttu-id="20967-114">Az utolsó parancs letiltja a biztonsági mentést az elemhez a \[ 0 $PI \] , de megtartja az adatot.</span><span class="sxs-lookup"><span data-stu-id="20967-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="20967-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20967-115">PARAMETERS</span></span>

### <span data-ttu-id="20967-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20967-116">-DefaultProfile</span></span>
<span data-ttu-id="20967-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20967-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20967-118">-Force</span><span class="sxs-lookup"><span data-stu-id="20967-118">-Force</span></span>
<span data-ttu-id="20967-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="20967-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="20967-120">-Elem</span><span class="sxs-lookup"><span data-stu-id="20967-120">-Item</span></span>
<span data-ttu-id="20967-121">Annak a biztonsági másolatnak az elemét adja meg, amelyre a parancsmag letiltja a védelmet.</span><span class="sxs-lookup"><span data-stu-id="20967-121">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="20967-122">Ha **AzureRmRecoveryServicesBackupItem** szeretne beolvasni, használja az Get-AzureRmRecoveryServicesBackupItem parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="20967-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: ItemBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20967-123">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="20967-123">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="20967-124">Azt jelzi, hogy ez a parancsmag törli a meglévő helyreállítási pontokat.</span><span class="sxs-lookup"><span data-stu-id="20967-124">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="20967-125">Ha később törölni szeretné a tárolt helyreállítási pontokat, futtassa újra ezt a parancsmagot, és adja meg ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="20967-125">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20967-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="20967-126">-Confirm</span></span>
<span data-ttu-id="20967-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="20967-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20967-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20967-128">-WhatIf</span></span>
<span data-ttu-id="20967-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="20967-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20967-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="20967-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20967-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20967-131">CommonParameters</span></span>
<span data-ttu-id="20967-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20967-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20967-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20967-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20967-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20967-134">INPUTS</span></span>

### <span data-ttu-id="20967-135">ItemBase</span><span class="sxs-lookup"><span data-stu-id="20967-135">ItemBase</span></span>
<span data-ttu-id="20967-136">A "tétel" paraméter értéke az "ItemBase" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="20967-136">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="20967-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20967-137">OUTPUTS</span></span>

### <span data-ttu-id="20967-138">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="20967-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="20967-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20967-139">NOTES</span></span>

## <span data-ttu-id="20967-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20967-140">RELATED LINKS</span></span>

[<span data-ttu-id="20967-141">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="20967-141">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="20967-142">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="20967-142">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="20967-143">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="20967-143">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


