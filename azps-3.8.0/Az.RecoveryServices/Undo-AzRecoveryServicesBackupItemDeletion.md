---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 80d03117278073b7b80b9c910a5ee4101a9db09a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011611"
---
# <span data-ttu-id="d26fe-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="d26fe-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="d26fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d26fe-102">SYNOPSIS</span></span>
<span data-ttu-id="d26fe-103">A finoman törölt elemek újrahidratálása</span><span class="sxs-lookup"><span data-stu-id="d26fe-103">Rehydrates a soft-deleted Item</span></span>

## <span data-ttu-id="d26fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d26fe-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d26fe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d26fe-105">DESCRIPTION</span></span>
<span data-ttu-id="d26fe-106">A Undo-AzRecoveryServicesBackupItemDeletion parancsmag újrahidratálja a finoman törölt elemeket.</span><span class="sxs-lookup"><span data-stu-id="d26fe-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet rehydrates a soft-deleted item.</span></span>
<span data-ttu-id="d26fe-107">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="d26fe-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d26fe-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d26fe-108">EXAMPLES</span></span>

### <span data-ttu-id="d26fe-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d26fe-109">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="d26fe-110">Az első parancs a biztonságimásolat-tárolók tömbjét kapja, majd a $Cont tömbben tárolja.</span><span class="sxs-lookup"><span data-stu-id="d26fe-110">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="d26fe-111">A második parancs az első tároló elemnek megfelelő biztonsági másolatot kapja, majd a $PI változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d26fe-111">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="d26fe-112">A harmadik parancs letiltja a biztonsági mentést $PI 0 elemen, \[ \] és egy softdeleted-állapotba helyezi az elemet.</span><span class="sxs-lookup"><span data-stu-id="d26fe-112">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="d26fe-113">A negyedik parancs az új elem, amely egy softdeleted-államban található.</span><span class="sxs-lookup"><span data-stu-id="d26fe-113">The fourth command the new item which is in a softdeleted state.</span></span>
<span data-ttu-id="d26fe-114">Az utolsó parancs hidratálja a softdeleted VM-et.</span><span class="sxs-lookup"><span data-stu-id="d26fe-114">The last command rehydrates the softdeleted VM.</span></span>

## <span data-ttu-id="d26fe-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d26fe-115">PARAMETERS</span></span>

### <span data-ttu-id="d26fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d26fe-116">-DefaultProfile</span></span>
<span data-ttu-id="d26fe-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d26fe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d26fe-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d26fe-118">-Force</span></span>
<span data-ttu-id="d26fe-119">Force – letiltja a biztonsági mentést (megelőzi a megerősítési párbeszédpanelt).</span><span class="sxs-lookup"><span data-stu-id="d26fe-119">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="d26fe-120">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="d26fe-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="d26fe-121">-Elem</span><span class="sxs-lookup"><span data-stu-id="d26fe-121">-Item</span></span>
<span data-ttu-id="d26fe-122">Annak a biztonsági másolatnak az elemét adja meg, amelyre a parancsmag letiltja a védelmet.</span><span class="sxs-lookup"><span data-stu-id="d26fe-122">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="d26fe-123">Ha AzureRmRecoveryServicesBackupItem szeretne beolvasni, használja az Get-AzRecoveryServicesBackupItem parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d26fe-123">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="d26fe-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d26fe-124">-VaultId</span></span>
<span data-ttu-id="d26fe-125">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="d26fe-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d26fe-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d26fe-126">-Confirm</span></span>
<span data-ttu-id="d26fe-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d26fe-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d26fe-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d26fe-128">-WhatIf</span></span>
<span data-ttu-id="d26fe-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d26fe-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d26fe-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d26fe-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d26fe-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d26fe-131">CommonParameters</span></span>
<span data-ttu-id="d26fe-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d26fe-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d26fe-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d26fe-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d26fe-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d26fe-134">INPUTS</span></span>

### <span data-ttu-id="d26fe-135">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="d26fe-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="d26fe-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d26fe-136">System.String</span></span>

## <span data-ttu-id="d26fe-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d26fe-137">OUTPUTS</span></span>

### <span data-ttu-id="d26fe-138">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="d26fe-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="d26fe-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d26fe-139">NOTES</span></span>

## <span data-ttu-id="d26fe-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d26fe-140">RELATED LINKS</span></span>

[<span data-ttu-id="d26fe-141">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="d26fe-141">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="d26fe-142">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d26fe-142">Get-AzRecoveryServicesBackupItem</span></span>]()

