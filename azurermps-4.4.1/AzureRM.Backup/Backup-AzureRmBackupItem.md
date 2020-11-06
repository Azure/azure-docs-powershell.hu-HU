---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9FF4F649-F50C-4C27-842F-1CD6C5BC7A2B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
ms.openlocfilehash: 1cb5ccf56a2ef6888231ca81df0e352f5d505e7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493587"
---
# <span data-ttu-id="06c89-101">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="06c89-101">Backup-AzureRmBackupItem</span></span>

## <span data-ttu-id="06c89-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06c89-102">SYNOPSIS</span></span>
<span data-ttu-id="06c89-103">Biztonságimásolat-elem biztonsági másolatának indítása</span><span class="sxs-lookup"><span data-stu-id="06c89-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06c89-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06c89-104">SYNTAX</span></span>

```
Backup-AzureRmBackupItem [-Item] <AzureRMBackupItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06c89-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="06c89-105">DESCRIPTION</span></span>
<span data-ttu-id="06c89-106">A **Backup-AzureRmBackupItem** parancsmag egy olyan védett Azure biztonsági másolat biztonsági másolatát indítja el, amely nincs a biztonsági ütemtervhez kötve.</span><span class="sxs-lookup"><span data-stu-id="06c89-106">The **Backup-AzureRmBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="06c89-107">A kezdeti biztonsági mentés után azonnal elvégezheti a biztonsági mentést, ha az ütemezett biztonsági mentés után nem tud biztonsági másolatot indítani.</span><span class="sxs-lookup"><span data-stu-id="06c89-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>

<span data-ttu-id="06c89-108">Ha egy meglévő biztonsági mentési feladat fut, ez a parancsmag nem hajtható végre.</span><span class="sxs-lookup"><span data-stu-id="06c89-108">If an existing backup job is running, this cmdlet fails.</span></span>

## <span data-ttu-id="06c89-109">Példák</span><span class="sxs-lookup"><span data-stu-id="06c89-109">EXAMPLES</span></span>

### <span data-ttu-id="06c89-110">1. példa: a virtuális gép biztonsági mentése</span><span class="sxs-lookup"><span data-stu-id="06c89-110">Example 1: Start to back up a virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container | Backup-AzureRmBackupItem
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
```

<span data-ttu-id="06c89-111">Az első parancs a Vault03 nevű boltozatot az Get-AzureRmBackupVault parancsmag segítségével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="06c89-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="06c89-112">A parancs az objektumot a $Vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="06c89-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="06c89-113">A második parancs egy olyan tárolót kap, amelyben a megadott név szerepel a boltozatban $Vault a Get-AzureRmBackupContainer parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="06c89-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="06c89-114">A parancs az objektumot a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="06c89-114">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="06c89-115">Az utolsó parancs a Get-AzureRmBackupItem parancsmag használatával kapja meg az $Container biztonsági mentési elemeit.</span><span class="sxs-lookup"><span data-stu-id="06c89-115">The last command gets the backup items in $Container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="06c89-116">A parancs a csővezeték-kezelő segítségével átadja az elemeket az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="06c89-116">The command passes the items to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="06c89-117">Az aktuális parancsmag a tárolóban lévő virtuális gép biztonsági mentését indítja el.</span><span class="sxs-lookup"><span data-stu-id="06c89-117">The current cmdlet starts backing up the virtual machine in the container.</span></span>

## <span data-ttu-id="06c89-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06c89-118">PARAMETERS</span></span>

### <span data-ttu-id="06c89-119">-Elem</span><span class="sxs-lookup"><span data-stu-id="06c89-119">-Item</span></span>
<span data-ttu-id="06c89-120">Annak a biztonságimásolat-elemnek a megadása, amelyhez ez a parancsmag elindítja a biztonsági mentési műveletet.</span><span class="sxs-lookup"><span data-stu-id="06c89-120">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06c89-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06c89-121">-DefaultProfile</span></span>
<span data-ttu-id="06c89-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06c89-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06c89-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06c89-123">CommonParameters</span></span>
<span data-ttu-id="06c89-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06c89-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06c89-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06c89-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06c89-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06c89-126">INPUTS</span></span>

### <span data-ttu-id="06c89-127">AzureRMBackupItem</span><span class="sxs-lookup"><span data-stu-id="06c89-127">AzureRMBackupItem</span></span>

## <span data-ttu-id="06c89-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06c89-128">OUTPUTS</span></span>

### <span data-ttu-id="06c89-129">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="06c89-129">AzureRmBackupJob</span></span>

## <span data-ttu-id="06c89-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06c89-130">NOTES</span></span>

## <span data-ttu-id="06c89-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06c89-131">RELATED LINKS</span></span>

[<span data-ttu-id="06c89-132">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="06c89-132">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="06c89-133">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="06c89-133">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="06c89-134">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="06c89-134">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)


