---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6187F603-5298-4854-94F3-0C38FCF3125F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
ms.openlocfilehash: f9f0808db919ad5d1d38b29daa720fb9b8a5baee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493867"
---
# <span data-ttu-id="e17a6-101">Get-AzureRmBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="e17a6-101">Get-AzureRmBackupJobDetails</span></span>

## <span data-ttu-id="e17a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e17a6-102">SYNOPSIS</span></span>
<span data-ttu-id="e17a6-103">A biztonsági mentési feladat részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e17a6-103">Gets the details of a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e17a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e17a6-104">SYNTAX</span></span>

### <span data-ttu-id="e17a6-105">JobsFiltersSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e17a6-105">JobsFiltersSet (Default)</span></span>
```
Get-AzureRmBackupJobDetails -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e17a6-106">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="e17a6-106">IdFiltersSet</span></span>
```
Get-AzureRmBackupJobDetails -Vault <AzureRMBackupVault> -JobId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e17a6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e17a6-107">DESCRIPTION</span></span>
<span data-ttu-id="e17a6-108">A **Get-AzureRmBackupJobDetails** parancsmag az Azure Backup-feladatok részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e17a6-108">The **Get-AzureRmBackupJobDetails** cmdlet gets the details of an Azure Backup job.</span></span>
<span data-ttu-id="e17a6-109">Ezzel a parancsmaggal információkat gyűjthet egy olyan projektről, amely nem működik.</span><span class="sxs-lookup"><span data-stu-id="e17a6-109">You can use this cmdlet to gather information about a job that fails.</span></span>

## <span data-ttu-id="e17a6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e17a6-110">EXAMPLES</span></span>

### <span data-ttu-id="e17a6-111">Példa 1: sikertelen munka részleteinek megjelenítése</span><span class="sxs-lookup"><span data-stu-id="e17a6-111">Example 1: Display the details of a failed job</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Jobs = Get-AzureRmBackupJob -Vault $Vault -Status Failed
PS C:\> $JobDetails = Get-AzureRmBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
ErrorCode ErrorMessage                            Recommendations
--------- ------------                            ---------------
   400001 Command execution failed.               {Another operation is currently in p...
```

<span data-ttu-id="e17a6-112">Az első parancs a Vault03 nevű boltozatot a **Get-AzureRmBackupVault** parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="e17a6-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="e17a6-113">A parancs az objektumot a $Vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e17a6-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="e17a6-114">A második parancs a $Vaultban a boltozattól sikertelen munkalapokat kap, majd a $Jobs Array változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="e17a6-114">The second command gets failed jobs from the vault in $Vault, and then stores them in the $Jobs array variable.</span></span>

<span data-ttu-id="e17a6-115">A harmadik feladat a $Jobs változó első feladatát részletezi, majd a $JobDetails változóban tárolja ezeket az adatokat.</span><span class="sxs-lookup"><span data-stu-id="e17a6-115">The third job gets details for the first job in the $Jobs variable, and then stores those details in the $JobDetails variable.</span></span>

<span data-ttu-id="e17a6-116">A végleges parancs az $JobDetails **ErrorDetails** tulajdonságát jeleníti meg normál pont szintaxis használatával.</span><span class="sxs-lookup"><span data-stu-id="e17a6-116">The final command displays the **ErrorDetails** property of $JobDetails by using standard dot syntax.</span></span>

### <span data-ttu-id="e17a6-117">2. példa: a sikertelen munka javasolt műveletének megjelenítése</span><span class="sxs-lookup"><span data-stu-id="e17a6-117">Example 2: Display the recommended action for a failed job</span></span>
```
PS C:\>$JobDetails.ErrorDetails.Recommendations
Another operation is currently in progress on this item. Please wait until the previous operation is completed, and then retry.
```

<span data-ttu-id="e17a6-118">Ez a parancs megjeleníti az első példában létrehozott $JobDetails változó javasolt műveletét.</span><span class="sxs-lookup"><span data-stu-id="e17a6-118">This command displays the recommended action from the $JobDetails variable that was created in the first example.</span></span>

## <span data-ttu-id="e17a6-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e17a6-119">PARAMETERS</span></span>

### <span data-ttu-id="e17a6-120">-Job</span><span class="sxs-lookup"><span data-stu-id="e17a6-120">-Job</span></span>
<span data-ttu-id="e17a6-121">Azt a feladatot adja meg, amelyre ez a parancsmag részletezi.</span><span class="sxs-lookup"><span data-stu-id="e17a6-121">Specifies a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="e17a6-122">**AzureRmBackupJob** objektum beolvasásához használja az Get-AzureRmBackupJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e17a6-122">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e17a6-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="e17a6-123">-JobId</span></span>
<span data-ttu-id="e17a6-124">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre ez a parancsmag részletezni kíván.</span><span class="sxs-lookup"><span data-stu-id="e17a6-124">Specifies the ID of a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="e17a6-125">Az azonosító egy **AzureRmBackupJob** objektum **InstanceId** tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="e17a6-125">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="e17a6-126">**AzureRmBackupJob** -objektum beszerzéséhez használja a Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="e17a6-126">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

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

### <span data-ttu-id="e17a6-127">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="e17a6-127">-Vault</span></span>
<span data-ttu-id="e17a6-128">Annak a biztonságimásolat-tárolónak a megadása, amelyhez ez a parancsmag munkahelyi adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="e17a6-128">Specifies the Backup vault for which this cmdlet gets job details.</span></span>
<span data-ttu-id="e17a6-129">**AzureRmBackupVault** objektum beolvasásához használja az Get-AzureRmBackupVault parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e17a6-129">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="e17a6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e17a6-130">-DefaultProfile</span></span>
<span data-ttu-id="e17a6-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e17a6-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e17a6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e17a6-132">CommonParameters</span></span>
<span data-ttu-id="e17a6-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e17a6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e17a6-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e17a6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e17a6-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e17a6-135">INPUTS</span></span>

### <span data-ttu-id="e17a6-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="e17a6-136">None</span></span>

## <span data-ttu-id="e17a6-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e17a6-137">OUTPUTS</span></span>

### <span data-ttu-id="e17a6-138">AzureRmBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="e17a6-138">AzureRmBackupJobDetails</span></span>

## <span data-ttu-id="e17a6-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e17a6-139">NOTES</span></span>
* <span data-ttu-id="e17a6-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="e17a6-140">None</span></span>

## <span data-ttu-id="e17a6-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e17a6-141">RELATED LINKS</span></span>

[<span data-ttu-id="e17a6-142">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="e17a6-142">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="e17a6-143">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="e17a6-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


