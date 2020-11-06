---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6778E018-B6CC-468A-823E-3DA047EA6B52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
ms.openlocfilehash: 0a5c5f42f7a6f4755335a5b8827fd2d23e096679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493862"
---
# <span data-ttu-id="0e000-101">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="0e000-101">Get-AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="0e000-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e000-102">SYNOPSIS</span></span>
<span data-ttu-id="0e000-103">A mentett elem helyreállítási pontjait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0e000-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e000-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e000-104">SYNTAX</span></span>

```
Get-AzureRmBackupRecoveryPoint [[-RecoveryPointId] <String>] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e000-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e000-105">DESCRIPTION</span></span>
<span data-ttu-id="0e000-106">A **Get-AzureRmBackupRecoveryPoint** parancsmag helyreállítási pontokat kap az Azure biztonsági másolat biztonsági másolatához.</span><span class="sxs-lookup"><span data-stu-id="0e000-106">The **Get-AzureRmBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="0e000-107">Egy elem biztonsági mentése után a biztonsági másolat egy vagy több helyreállítási pontot tárol.</span><span class="sxs-lookup"><span data-stu-id="0e000-107">After an item has been backed up, Backup stores one or more recovery points.</span></span>

## <span data-ttu-id="0e000-108">Példák</span><span class="sxs-lookup"><span data-stu-id="0e000-108">EXAMPLES</span></span>

### <span data-ttu-id="0e000-109">Példa 1: egy elem helyreállítási pontjainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="0e000-109">Example 1: Get recovery points for an item</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> Get-AzureRmBackupRecoveryPoint -Item $BackupItem
RecoveryPointId    RecoveryPointType  RecoveryPointTime      ContainerName
---------------    -----------------  -----------------      -------------
15273496567119     AppConsistent      26-Aug-15 12:27:38 PM  iaasvmcontainer;conto02-vm;conto0...
```

<span data-ttu-id="0e000-110">Az első parancs a Vault03 nevű boltozatot az Get-AzureRmBackupVault parancsmag segítségével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0e000-110">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="0e000-111">A parancs az objektumot a $Vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0e000-111">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="0e000-112">A második parancs a **Get-AzureRmBackupContainer** parancsmaggal egy olyan tárolót kap, amelyben a megadott név szerepel a boltozaton $Vault.</span><span class="sxs-lookup"><span data-stu-id="0e000-112">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="0e000-113">A parancs az objektumot a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0e000-113">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="0e000-114">A harmadik parancs a **Get-AzureRmBackupItem** parancsmag használatával kapja meg a biztonsági másolatot a $Container tárolójában.</span><span class="sxs-lookup"><span data-stu-id="0e000-114">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="0e000-115">A parancs az objektumot a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0e000-115">The command stores that object in the $BackupItem variable.</span></span>

<span data-ttu-id="0e000-116">A végleges parancs a $BackupItemban lévő elem helyreállítási pontját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0e000-116">The final command gets recovery points for the item in $BackupItem.</span></span>

## <span data-ttu-id="0e000-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e000-117">PARAMETERS</span></span>

### <span data-ttu-id="0e000-118">-Elem</span><span class="sxs-lookup"><span data-stu-id="0e000-118">-Item</span></span>
<span data-ttu-id="0e000-119">Annak az elemnek a meghatározása, amelyre a parancsmag helyreállítási pontokat kap.</span><span class="sxs-lookup"><span data-stu-id="0e000-119">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="0e000-120">Ha **AzureRmBackupItem** szeretne beolvasni, használja az Get-AzureRmBackupItem parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0e000-120">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="0e000-121">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="0e000-121">-RecoveryPointId</span></span>
<span data-ttu-id="0e000-122">Annak a helyreállítási pontnak az AZONOSÍTÓját adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="0e000-122">Specifies the ID of a recovery point that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e000-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e000-123">-DefaultProfile</span></span>
<span data-ttu-id="0e000-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0e000-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e000-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e000-125">CommonParameters</span></span>
<span data-ttu-id="0e000-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e000-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e000-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e000-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e000-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e000-128">INPUTS</span></span>

### <span data-ttu-id="0e000-129">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="0e000-129">AzureRmBackupItem</span></span>

## <span data-ttu-id="0e000-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e000-130">OUTPUTS</span></span>

### <span data-ttu-id="0e000-131">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="0e000-131">AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="0e000-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e000-132">NOTES</span></span>

## <span data-ttu-id="0e000-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e000-133">RELATED LINKS</span></span>

[<span data-ttu-id="0e000-134">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="0e000-134">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="0e000-135">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="0e000-135">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="0e000-136">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="0e000-136">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


