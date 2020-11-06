---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: DD150A2C-27D5-4119-9B43-FAB82F9F7D5B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
ms.openlocfilehash: c479869cb150633ca926542552fab2aa7dc80b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493578"
---
# <span data-ttu-id="cd994-101">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="cd994-101">Enable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="cd994-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd994-102">SYNOPSIS</span></span>
<span data-ttu-id="cd994-103">Egy elem társítása az Azure Backup Protection házirenddel</span><span class="sxs-lookup"><span data-stu-id="cd994-103">Associates an item with an Azure Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd994-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd994-104">SYNTAX</span></span>

```
Enable-AzureRmBackupProtection -Policy <AzureRMBackupProtectionPolicy>
 [-Item] <AzureRMBackupContainerContextObject> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd994-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd994-105">DESCRIPTION</span></span>
<span data-ttu-id="cd994-106">Az **enable-AzureRmBackupProtection** parancsmag egy, az Azure Backup Protection házirenddel rendelkező elemet társít.</span><span class="sxs-lookup"><span data-stu-id="cd994-106">The **Enable-AzureRmBackupProtection** cmdlet associates an item with an Azure Backup protection policy.</span></span>
<span data-ttu-id="cd994-107">A védelmi házirend engedélyezéséhez egy meglévő biztonsági elemmel és egy meglévő házirenddel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="cd994-107">To enable a protection policy, you must first have an existing backup item and an existing policy.</span></span>
<span data-ttu-id="cd994-108">Mindkettőnek ugyanahhoz a biztonságimásolat-tárolóhoz kell tartoznia.</span><span class="sxs-lookup"><span data-stu-id="cd994-108">Both must belong to the same Backup vault.</span></span>
<span data-ttu-id="cd994-109">A biztonsági mentés ütemezése az elem teljes eredeti példányát és a későbbi biztonsági mentések növekményes másolatát használja.</span><span class="sxs-lookup"><span data-stu-id="cd994-109">The backup schedule does the full initial copy for the item and the incremental copy for the subsequent backups.</span></span>

## <span data-ttu-id="cd994-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cd994-110">EXAMPLES</span></span>

### <span data-ttu-id="cd994-111">1. példa: védelem engedélyezése Azure virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="cd994-111">Example 1: Enable protection on an Azure virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Policy = Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered | Get-AzureRmBackupItem | Enable-AzureRmBackupProtection -Policy $Policy
WorkloadName    Operation        Status          StartTime              EndTime
------------    ---------        ------          ---------              -------
co03-vm         ConfigureBackup  Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
```

<span data-ttu-id="cd994-112">Az első parancs a Vault03 nevű boltozatot a **Get-AzureRmBackupVault** parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="cd994-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="cd994-113">A parancs az objektumot a $Vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cd994-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="cd994-114">A második parancs beolvassa a DefaultPolicy nevű biztonsági házirendet a $Vault boltozatához.</span><span class="sxs-lookup"><span data-stu-id="cd994-114">The second command gets the Backup protection policy named DefaultPolicy for the vault in $Vault.</span></span>
<span data-ttu-id="cd994-115">A parancs az objektumot a $Policy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cd994-115">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="cd994-116">A végleges parancs a pipeline operátorral adja át az értékeket az egyik parancsmagból a következőre.</span><span class="sxs-lookup"><span data-stu-id="cd994-116">The final command uses the pipeline operator to pass values from one cmdlet to the next.</span></span>
<span data-ttu-id="cd994-117">A Get-AzureRmBackupContainer parancsmag használatával kap egy tárolót.</span><span class="sxs-lookup"><span data-stu-id="cd994-117">It gets a container, by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="cd994-118">A parancs a Get-AzureRmBackupItem parancsmag használatával kapja meg az adott tároló biztonsági mentési elemét.</span><span class="sxs-lookup"><span data-stu-id="cd994-118">The command gets the backup item from that container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="cd994-119">Az aktuális parancsmag lehetővé teszi, hogy az $Policy-ban tárolt házirend a parancs által az adott parancsmaghoz átadott elemre kerüljön.</span><span class="sxs-lookup"><span data-stu-id="cd994-119">The current cmdlet enables the policy stored in $Policy for the item that the command passes to that cmdlet.</span></span>

## <span data-ttu-id="cd994-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd994-120">PARAMETERS</span></span>

### <span data-ttu-id="cd994-121">-Elem</span><span class="sxs-lookup"><span data-stu-id="cd994-121">-Item</span></span>
<span data-ttu-id="cd994-122">Annak a biztonsági másolatnak a biztonsági másolatát adja meg, amelyhez ez a parancsmag engedélyezi a védelmet.</span><span class="sxs-lookup"><span data-stu-id="cd994-122">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="cd994-123">Ha **AzureRmBackupItem** szeretne beolvasni, használja az Get-AzureRmBackupItem parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cd994-123">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainerContextObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd994-124">-Házirend</span><span class="sxs-lookup"><span data-stu-id="cd994-124">-Policy</span></span>
<span data-ttu-id="cd994-125">Azt a védelmi házirendet adja meg, amelyet a parancsmag társít egy elemhez.</span><span class="sxs-lookup"><span data-stu-id="cd994-125">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="cd994-126">**AzureRmBackupProtectionPolicy** objektum beolvasásához használja az Get-AzureRmBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cd994-126">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd994-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd994-127">-DefaultProfile</span></span>
<span data-ttu-id="cd994-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd994-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd994-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd994-129">CommonParameters</span></span>
<span data-ttu-id="cd994-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd994-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd994-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd994-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd994-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd994-132">INPUTS</span></span>

### <span data-ttu-id="cd994-133">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="cd994-133">AzureRmBackupItem</span></span>

## <span data-ttu-id="cd994-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd994-134">OUTPUTS</span></span>

### <span data-ttu-id="cd994-135">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="cd994-135">AzureRmBackupJob</span></span>

## <span data-ttu-id="cd994-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd994-136">NOTES</span></span>

## <span data-ttu-id="cd994-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd994-137">RELATED LINKS</span></span>

[<span data-ttu-id="cd994-138">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="cd994-138">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="cd994-139">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="cd994-139">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="cd994-140">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="cd994-140">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)


