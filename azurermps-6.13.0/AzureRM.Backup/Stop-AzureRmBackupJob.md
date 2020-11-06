---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 44C5AF58-ADC1-4BC6-9771-3FD8F0480106
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/stop-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
ms.openlocfilehash: 800b5c6e04e0842113db7fb3494815bcd97ebfb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494170"
---
# <span data-ttu-id="d7be6-101">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="d7be6-101">Stop-AzureRmBackupJob</span></span>

## <span data-ttu-id="d7be6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7be6-102">SYNOPSIS</span></span>
<span data-ttu-id="d7be6-103">Visszavon egy meglévő biztonsági mentési feladatot.</span><span class="sxs-lookup"><span data-stu-id="d7be6-103">Cancels an existing Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7be6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7be6-104">SYNTAX</span></span>

### <span data-ttu-id="d7be6-105">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="d7be6-105">IdFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Vault <AzureRMBackupVault> -JobID <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7be6-106">JobFiltersSet</span><span class="sxs-lookup"><span data-stu-id="d7be6-106">JobFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7be6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7be6-107">DESCRIPTION</span></span>
<span data-ttu-id="d7be6-108">A **stop-AzureRmBackupJob** parancsmag lemond egy meglévő Azure biztonsági mentési feladatról.</span><span class="sxs-lookup"><span data-stu-id="d7be6-108">The **Stop-AzureRmBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="d7be6-109">Ezzel a paraméterrel leállíthat egy olyan feladatot, amely túl sokáig tart, és más tevékenységeket is blokkol.</span><span class="sxs-lookup"><span data-stu-id="d7be6-109">Use this parameter to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="d7be6-110">Csak az alábbi típusú feladatokat lehet lemondani:</span><span class="sxs-lookup"><span data-stu-id="d7be6-110">You can cancel only the following types of jobs:</span></span> 
- <span data-ttu-id="d7be6-111">Hát</span><span class="sxs-lookup"><span data-stu-id="d7be6-111">Backup</span></span>
- <span data-ttu-id="d7be6-112">Visszaállítása</span><span class="sxs-lookup"><span data-stu-id="d7be6-112">Restore</span></span>

## <span data-ttu-id="d7be6-113">Példák</span><span class="sxs-lookup"><span data-stu-id="d7be6-113">EXAMPLES</span></span>

### <span data-ttu-id="d7be6-114">Példa 1: biztonsági mentési feladat leállítása a projekt AZONOSÍTÓjának használatával</span><span class="sxs-lookup"><span data-stu-id="d7be6-114">Example 1: Stop a backup job by using a job ID</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Job = Get-AzureRmBackupJob -Vault $Vault -Operation Backup
PS C:\> Stop-AzureRmBackupJob -Vault $Vault -JobID $Job.InstanceId
```

<span data-ttu-id="d7be6-115">Az első parancs a Vault03 nevű boltozatot a **Get-AzureRmBackupVault** parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="d7be6-115">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="d7be6-116">A parancs az objektumot a $Vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d7be6-116">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="d7be6-117">A második parancs a **Get-AzureRmBackupJob** parancsmagból kapja meg a biztonsági mentési feladatot $Vault a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="d7be6-117">The second command gets a backup job from the vault in $Vault by using the **Get-AzureRmBackupJob** cmdlet.</span></span>
<span data-ttu-id="d7be6-118">A parancs a $Job változóban tárolja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="d7be6-118">The command stores the job in the $Job variable.</span></span>
<span data-ttu-id="d7be6-119">Ebben a példában csak egy biztonsági művelet van megadva a megadott boltozaton.</span><span class="sxs-lookup"><span data-stu-id="d7be6-119">In this example, there is only one backup operation in the specified vault.</span></span>
<span data-ttu-id="d7be6-120">A végleges parancs leállítja a megadott azonosítót tartalmazó munkát.</span><span class="sxs-lookup"><span data-stu-id="d7be6-120">The final command stops the job that has the specified ID.</span></span>

### <span data-ttu-id="d7be6-121">2. példa: az összes visszaállítási művelet leállítása</span><span class="sxs-lookup"><span data-stu-id="d7be6-121">Example 2: Stop all Restore operations</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Operation Restore | Stop-AzureRmBackupJob
```

<span data-ttu-id="d7be6-122">Ez a parancs beolvassa az összes visszaállítási műveletet a boltozaton $Vault, majd a pipeline operátor segítségével átadja őket az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="d7be6-122">This command gets all the restore operations in the vault in $Vault, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d7be6-123">Az aktuális parancsmag minden feladatot leáll.</span><span class="sxs-lookup"><span data-stu-id="d7be6-123">The current cmdlet stops each job.</span></span>

## <span data-ttu-id="d7be6-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7be6-124">PARAMETERS</span></span>

### <span data-ttu-id="d7be6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7be6-125">-DefaultProfile</span></span>
<span data-ttu-id="d7be6-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d7be6-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7be6-127">-Job</span><span class="sxs-lookup"><span data-stu-id="d7be6-127">-Job</span></span>
<span data-ttu-id="d7be6-128">A parancsmag által lemondott feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7be6-128">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="d7be6-129">**AzureRmBackupJob** objektum beolvasásához használja az Get-AzureRmBackupJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d7be6-129">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="d7be6-130">-JobID</span><span class="sxs-lookup"><span data-stu-id="d7be6-130">-JobID</span></span>
<span data-ttu-id="d7be6-131">A parancsmag által lemondott feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7be6-131">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="d7be6-132">**AzureRmBackupJob** objektum beolvasásához használja az Get-AzureRmBackupJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d7be6-132">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="d7be6-133">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="d7be6-133">-Vault</span></span>
<span data-ttu-id="d7be6-134">Annak a biztonságimásolat-tárolónak a megadása, amelyben ez a parancsmag lemond egy feladatot.</span><span class="sxs-lookup"><span data-stu-id="d7be6-134">Specifies the Backup vault in which this cmdlet cancels a job.</span></span>
<span data-ttu-id="d7be6-135">**AzureRmBackupVault** objektum beolvasásához használja az Get-AzureRmBackupVault parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d7be6-135">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="d7be6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7be6-136">CommonParameters</span></span>
<span data-ttu-id="d7be6-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7be6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7be6-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7be6-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7be6-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7be6-139">INPUTS</span></span>

### <span data-ttu-id="d7be6-140">Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="d7be6-140">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>
<span data-ttu-id="d7be6-141">Paraméterek: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d7be6-141">Parameters: Job (ByValue)</span></span>

## <span data-ttu-id="d7be6-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7be6-142">OUTPUTS</span></span>

### <span data-ttu-id="d7be6-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="d7be6-143">System.Void</span></span>

## <span data-ttu-id="d7be6-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7be6-144">NOTES</span></span>

## <span data-ttu-id="d7be6-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7be6-145">RELATED LINKS</span></span>

[<span data-ttu-id="d7be6-146">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="d7be6-146">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="d7be6-147">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d7be6-147">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="d7be6-148">Várjon-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="d7be6-148">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


