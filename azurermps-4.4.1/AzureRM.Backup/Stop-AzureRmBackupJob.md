---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 44C5AF58-ADC1-4BC6-9771-3FD8F0480106
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
ms.openlocfilehash: d502596b8c5ddde576b5fd22ee31398b2c4e869a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504228"
---
# <span data-ttu-id="12a45-101">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="12a45-101">Stop-AzureRmBackupJob</span></span>

## <span data-ttu-id="12a45-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="12a45-102">SYNOPSIS</span></span>
<span data-ttu-id="12a45-103">Visszavon egy meglévő biztonsági mentési feladatot.</span><span class="sxs-lookup"><span data-stu-id="12a45-103">Cancels an existing Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12a45-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="12a45-104">SYNTAX</span></span>

### <span data-ttu-id="12a45-105">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="12a45-105">IdFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Vault <AzureRMBackupVault> -JobID <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12a45-106">JobFiltersSet</span><span class="sxs-lookup"><span data-stu-id="12a45-106">JobFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12a45-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="12a45-107">DESCRIPTION</span></span>
<span data-ttu-id="12a45-108">A **stop-AzureRmBackupJob** parancsmag lemond egy meglévő Azure biztonsági mentési feladatról.</span><span class="sxs-lookup"><span data-stu-id="12a45-108">The **Stop-AzureRmBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="12a45-109">Ezzel a paraméterrel leállíthat egy olyan feladatot, amely túl sokáig tart, és más tevékenységeket is blokkol.</span><span class="sxs-lookup"><span data-stu-id="12a45-109">Use this parameter to stop a job that takes too long and blocks other activities.</span></span>

<span data-ttu-id="12a45-110">Csak az alábbi típusú feladatokat lehet lemondani:</span><span class="sxs-lookup"><span data-stu-id="12a45-110">You can cancel only the following types of jobs:</span></span> 

- <span data-ttu-id="12a45-111">Hát</span><span class="sxs-lookup"><span data-stu-id="12a45-111">Backup</span></span>
- <span data-ttu-id="12a45-112">Visszaállítása</span><span class="sxs-lookup"><span data-stu-id="12a45-112">Restore</span></span>

## <span data-ttu-id="12a45-113">Példák</span><span class="sxs-lookup"><span data-stu-id="12a45-113">EXAMPLES</span></span>

### <span data-ttu-id="12a45-114">Példa 1: biztonsági mentési feladat leállítása a projekt AZONOSÍTÓjának használatával</span><span class="sxs-lookup"><span data-stu-id="12a45-114">Example 1: Stop a backup job by using a job ID</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Job = Get-AzureRmBackupJob -Vault $Vault -Operation Backup
PS C:\> Stop-AzureRmBackupJob -Vault $Vault -JobID $Job.InstanceId
```

<span data-ttu-id="12a45-115">Az első parancs a Vault03 nevű boltozatot a **Get-AzureRmBackupVault** parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="12a45-115">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="12a45-116">A parancs az objektumot a $Vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="12a45-116">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="12a45-117">A második parancs a **Get-AzureRmBackupJob** parancsmagból kapja meg a biztonsági mentési feladatot $Vault a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="12a45-117">The second command gets a backup job from the vault in $Vault by using the **Get-AzureRmBackupJob** cmdlet.</span></span>
<span data-ttu-id="12a45-118">A parancs a $Job változóban tárolja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="12a45-118">The command stores the job in the $Job variable.</span></span>
<span data-ttu-id="12a45-119">Ebben a példában csak egy biztonsági művelet van megadva a megadott boltozaton.</span><span class="sxs-lookup"><span data-stu-id="12a45-119">In this example, there is only one backup operation in the specified vault.</span></span>

<span data-ttu-id="12a45-120">A végleges parancs leállítja a megadott azonosítót tartalmazó munkát.</span><span class="sxs-lookup"><span data-stu-id="12a45-120">The final command stops the job that has the specified ID.</span></span>

### <span data-ttu-id="12a45-121">2. példa: az összes visszaállítási művelet leállítása</span><span class="sxs-lookup"><span data-stu-id="12a45-121">Example 2: Stop all Restore operations</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Operation Restore | Stop-AzureRmBackupJob
```

<span data-ttu-id="12a45-122">Ez a parancs beolvassa az összes visszaállítási műveletet a boltozaton $Vault, majd a pipeline operátor segítségével átadja őket az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="12a45-122">This command gets all the restore operations in the vault in $Vault, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="12a45-123">Az aktuális parancsmag minden feladatot leáll.</span><span class="sxs-lookup"><span data-stu-id="12a45-123">The current cmdlet stops each job.</span></span>

## <span data-ttu-id="12a45-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="12a45-124">PARAMETERS</span></span>

### <span data-ttu-id="12a45-125">-Job</span><span class="sxs-lookup"><span data-stu-id="12a45-125">-Job</span></span>
<span data-ttu-id="12a45-126">A parancsmag által lemondott feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="12a45-126">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="12a45-127">**AzureRmBackupJob** objektum beolvasásához használja az Get-AzureRmBackupJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="12a45-127">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12a45-128">-JobID</span><span class="sxs-lookup"><span data-stu-id="12a45-128">-JobID</span></span>
<span data-ttu-id="12a45-129">A parancsmag által lemondott feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="12a45-129">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="12a45-130">**AzureRmBackupJob** objektum beolvasásához használja az Get-AzureRmBackupJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="12a45-130">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a45-131">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="12a45-131">-Vault</span></span>
<span data-ttu-id="12a45-132">Annak a biztonságimásolat-tárolónak a megadása, amelyben ez a parancsmag lemond egy feladatot.</span><span class="sxs-lookup"><span data-stu-id="12a45-132">Specifies the Backup vault in which this cmdlet cancels a job.</span></span>
<span data-ttu-id="12a45-133">**AzureRmBackupVault** objektum beolvasásához használja az Get-AzureRmBackupVault parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="12a45-133">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a45-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a45-134">-DefaultProfile</span></span>
<span data-ttu-id="12a45-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="12a45-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12a45-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a45-136">CommonParameters</span></span>
<span data-ttu-id="12a45-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="12a45-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a45-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12a45-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a45-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="12a45-139">INPUTS</span></span>

### <span data-ttu-id="12a45-140">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="12a45-140">AzureRmBackupJob</span></span>

## <span data-ttu-id="12a45-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12a45-141">OUTPUTS</span></span>

### <span data-ttu-id="12a45-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="12a45-142">None</span></span>

## <span data-ttu-id="12a45-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="12a45-143">NOTES</span></span>

## <span data-ttu-id="12a45-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12a45-144">RELATED LINKS</span></span>

[<span data-ttu-id="12a45-145">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="12a45-145">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="12a45-146">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="12a45-146">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="12a45-147">Várjon-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="12a45-147">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


