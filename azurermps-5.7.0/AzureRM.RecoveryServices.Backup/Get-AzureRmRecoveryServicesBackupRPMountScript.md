---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 0f3f0292b4f348207bf80d5e04c63dc45be69fa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493072"
---
# <span data-ttu-id="50146-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="50146-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="50146-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="50146-102">SYNOPSIS</span></span>
<span data-ttu-id="50146-103">Letölthet egy parancsfájlt a helyreállítási pont összes fájljának csatlakoztatásához.</span><span class="sxs-lookup"><span data-stu-id="50146-103">Downloads a script to mount all the files of the recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50146-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="50146-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50146-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="50146-105">DESCRIPTION</span></span>
<span data-ttu-id="50146-106">A Get-AzureRmRecoveryServicesBackupRPMountScript parancsmag letölthet egy parancsfájlt, amely a futtatott számítógépen a helyreállítási pont mennyiségét csatolja.</span><span class="sxs-lookup"><span data-stu-id="50146-106">The Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet downloads a script which mounts the volumes of the recovery point on the machine where it is run.</span></span>

## <span data-ttu-id="50146-107">Példák</span><span class="sxs-lookup"><span data-stu-id="50146-107">EXAMPLES</span></span>

### <span data-ttu-id="50146-108">1. példa: helyreállítási pont csatlakoztatása</span><span class="sxs-lookup"><span data-stu-id="50146-108">Example 1: Mount a recovery point</span></span>
```
PS C:\> $namedContainer = Get-AzureRmRecoveryServicesBackupContainer  -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM"
PS C:\> $backupitem = Get-AzureRmRecoveryServicesBackupItem -Container $namedContainer  -WorkloadType "AzureVM"
PS C:\> $startDate = (Get-Date).AddDays(-7)
PS C:\> $endDate = Get-Date
PS C:\> $rp = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $backupitem -StartDate $startdate.ToUniversalTime() -EndDate $enddate.ToUniversalTime()

To mount files of the latest recovery point, obtain the script by

PS C:\> Get-AzureRmRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]

OsType  Password        Filename
------  --------        --------
Windows e3632984e51f496 V2VM_wus2_8287309959960546283_451516692429_cbd6061f7fc543c489f1974d33659fed07a6e0c2e08740.exe
```

<span data-ttu-id="50146-109">A parancsfájl futtatásakor a helyreállítási pont fájljait fogja csatlakoztatni $rp \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="50146-109">When the script is run, it will mount the files of the recovery point $rp\[0\]</span></span>

## <span data-ttu-id="50146-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="50146-110">PARAMETERS</span></span>

### <span data-ttu-id="50146-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50146-111">-DefaultProfile</span></span>
<span data-ttu-id="50146-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="50146-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50146-113">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="50146-113">-Path</span></span>
<span data-ttu-id="50146-114">Annak a helynek a helye, ahol a fájl a fájl helyreállítása esetén letölthető.</span><span class="sxs-lookup"><span data-stu-id="50146-114">Location where the file should be downloaded in the case of file recovery.</span></span> <span data-ttu-id="50146-115">Ha az elérési út nincs megadva, a parancsfájl a fájlt az aktuális könyvtárba fogja letölteni.</span><span class="sxs-lookup"><span data-stu-id="50146-115">If -Path is not provided, the script file will be downloaded in the current directory.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50146-116">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="50146-116">-RecoveryPoint</span></span>
<span data-ttu-id="50146-117">Visszaállítandó helyreállítási pont objektum</span><span class="sxs-lookup"><span data-stu-id="50146-117">Recovery point object to be restored</span></span>

```yaml
Type: RecoveryPointBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50146-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="50146-118">-Confirm</span></span>
<span data-ttu-id="50146-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="50146-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50146-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50146-120">-WhatIf</span></span>
<span data-ttu-id="50146-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="50146-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50146-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="50146-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50146-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50146-123">CommonParameters</span></span>
<span data-ttu-id="50146-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="50146-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50146-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50146-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50146-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="50146-126">INPUTS</span></span>

### <span data-ttu-id="50146-127">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="50146-127">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="50146-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50146-128">OUTPUTS</span></span>

### <span data-ttu-id="50146-129">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RPMountScriptDetails</span><span class="sxs-lookup"><span data-stu-id="50146-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RPMountScriptDetails</span></span>

## <span data-ttu-id="50146-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="50146-130">NOTES</span></span>

## <span data-ttu-id="50146-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50146-131">RELATED LINKS</span></span>

