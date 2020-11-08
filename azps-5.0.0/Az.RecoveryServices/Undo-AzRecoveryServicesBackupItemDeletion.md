---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 62d8dc302dc5819272034cfdd1c3fd0c0c79f54c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186845"
---
# <span data-ttu-id="cdc28-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="cdc28-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="cdc28-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cdc28-102">SYNOPSIS</span></span>
<span data-ttu-id="cdc28-103">Ha egy biztonságimásolat-elem törlődik, és egy finoman törölt állapotban van, ez a parancs visszaállítja azt az állapotot, ahol az adat örökre megmarad</span><span class="sxs-lookup"><span data-stu-id="cdc28-103">If a backup item is deleted and present in a soft-deleted state, this command brings the item back to a state where the data is retained forever</span></span> 

## <span data-ttu-id="cdc28-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cdc28-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdc28-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cdc28-105">DESCRIPTION</span></span>
<span data-ttu-id="cdc28-106">A Undo-AzRecoveryServicesBackupItemDeletion parancsmag egy olyan állapotra állítja vissza a finoman törölt elemeket, amelyben a védelem le van állítva, az adatmegőrzés azonban örökké megmarad.</span><span class="sxs-lookup"><span data-stu-id="cdc28-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet reverts a soft-deleted item to a state where the protection is stopped but data is retained forever.</span></span>

## <span data-ttu-id="cdc28-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cdc28-107">EXAMPLES</span></span>

### <span data-ttu-id="cdc28-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cdc28-108">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM | Where-Object {$_.DeleteState -eq "ToBeDeleted"}
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="cdc28-109">Az első parancs a biztonságimásolat-tárolók tömbjét kapja, majd a $Cont tömbben tárolja.</span><span class="sxs-lookup"><span data-stu-id="cdc28-109">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="cdc28-110">A második parancs az első tároló elemnek megfelelő biztonsági másolatot kapja, majd a $PI változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cdc28-110">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="cdc28-111">A harmadik parancs letiltja a biztonsági mentést $PI 0 elemen, \[ \] és egy softdeleted-állapotba helyezi az elemet.</span><span class="sxs-lookup"><span data-stu-id="cdc28-111">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="cdc28-112">A negyedik parancs a softdeleted-állapotot tartalmazó elemet kapja.</span><span class="sxs-lookup"><span data-stu-id="cdc28-112">The fourth command gets the item which is in a softdeleted state.</span></span>
<span data-ttu-id="cdc28-113">Az utolsó parancs a softdeleted VM-et egy olyan államba hozza létre, ahol a védelem megszűnt, az adatmegőrzés azonban örökké megmarad.</span><span class="sxs-lookup"><span data-stu-id="cdc28-113">The last command brings the softdeleted VM to a state where the protection is stopped but data is retained forever.</span></span>

### <span data-ttu-id="cdc28-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="cdc28-114">Example 2</span></span>

<span data-ttu-id="cdc28-115">Újrahidratálja a finoman törölt elemeket.</span><span class="sxs-lookup"><span data-stu-id="cdc28-115">Rehydrates a soft-deleted Item.</span></span> <span data-ttu-id="cdc28-116">autogenerated</span><span class="sxs-lookup"><span data-stu-id="cdc28-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0] -VaultId $vault.ID
```

## <span data-ttu-id="cdc28-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cdc28-117">PARAMETERS</span></span>

### <span data-ttu-id="cdc28-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdc28-118">-DefaultProfile</span></span>
<span data-ttu-id="cdc28-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cdc28-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdc28-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cdc28-120">-Force</span></span>
<span data-ttu-id="cdc28-121">Force – letiltja a biztonsági mentést (megelőzi a megerősítési párbeszédpanelt).</span><span class="sxs-lookup"><span data-stu-id="cdc28-121">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="cdc28-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="cdc28-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="cdc28-123">-Elem</span><span class="sxs-lookup"><span data-stu-id="cdc28-123">-Item</span></span>
<span data-ttu-id="cdc28-124">Annak a biztonsági mentési elemnek a meghatározása, amelyre a parancsmag visszaállítja a törlést.</span><span class="sxs-lookup"><span data-stu-id="cdc28-124">Specifies the backup item for which this cmdlet reverts the deletion.</span></span>
<span data-ttu-id="cdc28-125">Ha AzureRmRecoveryServicesBackupItem szeretne beolvasni, használja az Get-AzRecoveryServicesBackupItem parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cdc28-125">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="cdc28-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="cdc28-126">-VaultId</span></span>
<span data-ttu-id="cdc28-127">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="cdc28-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="cdc28-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cdc28-128">-Confirm</span></span>
<span data-ttu-id="cdc28-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cdc28-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdc28-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdc28-130">-WhatIf</span></span>
<span data-ttu-id="cdc28-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cdc28-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdc28-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cdc28-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdc28-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdc28-133">CommonParameters</span></span>
<span data-ttu-id="cdc28-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cdc28-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdc28-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cdc28-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdc28-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdc28-136">INPUTS</span></span>

### <span data-ttu-id="cdc28-137">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="cdc28-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="cdc28-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cdc28-138">System.String</span></span>

## <span data-ttu-id="cdc28-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdc28-139">OUTPUTS</span></span>

### <span data-ttu-id="cdc28-140">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="cdc28-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="cdc28-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cdc28-141">NOTES</span></span>

## <span data-ttu-id="cdc28-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cdc28-142">RELATED LINKS</span></span>

[<span data-ttu-id="cdc28-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="cdc28-143">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="cdc28-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="cdc28-144">Get-AzRecoveryServicesBackupItem</span></span>]()

