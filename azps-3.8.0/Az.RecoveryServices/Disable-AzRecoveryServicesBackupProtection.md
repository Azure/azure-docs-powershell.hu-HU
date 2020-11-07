---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: d0b2d15b3f2515969e423e8ac8d019a1413fcad7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847126"
---
# <span data-ttu-id="2877e-101">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="2877e-101">Disable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="2877e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2877e-102">SYNOPSIS</span></span>
<span data-ttu-id="2877e-103">Letiltja a biztonsági mentéssel védett elemek védelmét.</span><span class="sxs-lookup"><span data-stu-id="2877e-103">Disables protection for a Backup-protected item.</span></span>

## <span data-ttu-id="2877e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2877e-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2877e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2877e-105">DESCRIPTION</span></span>
<span data-ttu-id="2877e-106">A **disable-AzRecoveryServicesBackupProtection** parancsmag letiltja az Azure biztonsági másolattal védett elemek védelmét.</span><span class="sxs-lookup"><span data-stu-id="2877e-106">The **Disable-AzRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="2877e-107">Ez a parancsmag leállítja az elemek rendszeres ütemezett biztonsági mentését.</span><span class="sxs-lookup"><span data-stu-id="2877e-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="2877e-108">Ez a parancsmag a biztonsági másolat meglévő helyreállítási pontját is törölheti.</span><span class="sxs-lookup"><span data-stu-id="2877e-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>
<span data-ttu-id="2877e-109">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="2877e-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="2877e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2877e-110">EXAMPLES</span></span>

### <span data-ttu-id="2877e-111">1. példa: biztonsági másolat elleni védelem letiltása</span><span class="sxs-lookup"><span data-stu-id="2877e-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="2877e-112">Az első parancs a biztonságimásolat-tárolók tömbjét kapja, majd a $Cont tömbben tárolja.</span><span class="sxs-lookup"><span data-stu-id="2877e-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="2877e-113">A második parancs az első tároló elemnek megfelelő biztonsági másolatot kapja, majd a $PI változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2877e-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="2877e-114">Az utolsó parancs letiltja a biztonsági mentést az elemhez a \[ 0 $PI \] , de megtartja az adatot.</span><span class="sxs-lookup"><span data-stu-id="2877e-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="2877e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2877e-115">PARAMETERS</span></span>

### <span data-ttu-id="2877e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2877e-116">-DefaultProfile</span></span>
<span data-ttu-id="2877e-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2877e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2877e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2877e-118">-Force</span></span>
<span data-ttu-id="2877e-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="2877e-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2877e-120">-Elem</span><span class="sxs-lookup"><span data-stu-id="2877e-120">-Item</span></span>
<span data-ttu-id="2877e-121">Annak a biztonsági másolatnak az elemét adja meg, amelyre a parancsmag letiltja a védelmet.</span><span class="sxs-lookup"><span data-stu-id="2877e-121">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="2877e-122">Ha **AzureRmRecoveryServicesBackupItem** szeretne beolvasni, használja az Get-AzRecoveryServicesBackupItem parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2877e-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2877e-123">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="2877e-123">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="2877e-124">Azt jelzi, hogy ez a parancsmag törli a meglévő helyreállítási pontokat.</span><span class="sxs-lookup"><span data-stu-id="2877e-124">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="2877e-125">Ha később törölni szeretné a tárolt helyreállítási pontokat, futtassa újra ezt a parancsmagot, és adja meg ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="2877e-125">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2877e-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2877e-126">-VaultId</span></span>
<span data-ttu-id="2877e-127">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="2877e-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2877e-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2877e-128">-Confirm</span></span>
<span data-ttu-id="2877e-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2877e-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2877e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2877e-130">-WhatIf</span></span>
<span data-ttu-id="2877e-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2877e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2877e-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2877e-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2877e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2877e-133">CommonParameters</span></span>
<span data-ttu-id="2877e-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2877e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2877e-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2877e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2877e-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2877e-136">INPUTS</span></span>

### <span data-ttu-id="2877e-137">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="2877e-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="2877e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2877e-138">System.String</span></span>

## <span data-ttu-id="2877e-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2877e-139">OUTPUTS</span></span>

### <span data-ttu-id="2877e-140">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="2877e-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="2877e-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2877e-141">NOTES</span></span>

## <span data-ttu-id="2877e-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2877e-142">RELATED LINKS</span></span>

[<span data-ttu-id="2877e-143">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="2877e-143">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="2877e-144">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="2877e-144">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="2877e-145">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="2877e-145">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


