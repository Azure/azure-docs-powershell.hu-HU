---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: ef4d8ca2e1fb21165281375b3d325f5fc8b6ceed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493861"
---
# <span data-ttu-id="cabc4-101">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="cabc4-101">Get-AzureRmBackupVault</span></span>

## <span data-ttu-id="cabc4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cabc4-102">SYNOPSIS</span></span>
<span data-ttu-id="cabc4-103">Biztonsági mentési boltozatokat kap.</span><span class="sxs-lookup"><span data-stu-id="cabc4-103">Gets Backup vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cabc4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cabc4-104">SYNTAX</span></span>

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cabc4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cabc4-105">DESCRIPTION</span></span>
<span data-ttu-id="cabc4-106">A **Get-AzureRmBackupVault** parancsmag Azure Backup-boltozatokat kap.</span><span class="sxs-lookup"><span data-stu-id="cabc4-106">The **Get-AzureRmBackupVault** cmdlet gets Azure Backup vaults.</span></span>
<span data-ttu-id="cabc4-107">Ez a parancsmag a más parancsmagokkal használható **AzureRmBackupVault** -objektumokat számítja ki.</span><span class="sxs-lookup"><span data-stu-id="cabc4-107">This cmdlet returns **AzureRmBackupVault** objects for use with other cmdlets.</span></span>

## <span data-ttu-id="cabc4-108">Példák</span><span class="sxs-lookup"><span data-stu-id="cabc4-108">EXAMPLES</span></span>

### <span data-ttu-id="cabc4-109">Példa 1: az összes biztonságimásolat-boltozat megtekintése</span><span class="sxs-lookup"><span data-stu-id="cabc4-109">Example 1: View all the Backup vaults</span></span>
```
PS C:\>Get-AzureRmBackupVault
```

<span data-ttu-id="cabc4-110">Ez a parancs minden Azure biztonságimásolat-tárolót kap.</span><span class="sxs-lookup"><span data-stu-id="cabc4-110">This command gets all the Azure Backup vaults.</span></span>

### <span data-ttu-id="cabc4-111">2. példa: a West US-ban létrehozott összes boltozat megtekintése</span><span class="sxs-lookup"><span data-stu-id="cabc4-111">Example 2: View all vaults created in West US</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

<span data-ttu-id="cabc4-112">Ez a parancs a biztonságimásolat-tárolókat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cabc4-112">This command gets all the Backup vaults.</span></span>
<span data-ttu-id="cabc4-113">A parancs a csővezeték-kezelő segítségével átadja őket a Where-Object parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="cabc4-113">The command passes them to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cabc4-114">Az adott parancsmag a **régió** tulajdonság alapján szűri az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="cabc4-114">That cmdlet filters the results based on the **Region** property.</span></span>
<span data-ttu-id="cabc4-115">További információért írja be a következőt: `Get-Help Where-Object` .</span><span class="sxs-lookup"><span data-stu-id="cabc4-115">For more information, type `Get-Help Where-Object`.</span></span>

### <span data-ttu-id="cabc4-116">3. példa: speciális boltozat beszerzése</span><span class="sxs-lookup"><span data-stu-id="cabc4-116">Example 3: Get a specific vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="cabc4-117">Ez a parancs a Vault03 nevű boltozatot kapja.</span><span class="sxs-lookup"><span data-stu-id="cabc4-117">This command gets the vault named Vault03.</span></span>

### <span data-ttu-id="cabc4-118">Példa 4: a helyileg redundáns tárterületet tartalmazó boltozatok számának megszámolása</span><span class="sxs-lookup"><span data-stu-id="cabc4-118">Example 4: Count the number of vaults that have locally redundant storage</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

<span data-ttu-id="cabc4-119">Ez a parancs minden Azure biztonságimásolat-tárolót kap.</span><span class="sxs-lookup"><span data-stu-id="cabc4-119">This command gets all the Azure Backup vaults.</span></span>
<span data-ttu-id="cabc4-120">A parancs átadja azokat a **Where-Object** értékre, amely a **tárolási** tulajdonság alapján szűri az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="cabc4-120">The command passes them to **Where-Object** , which filters the results based on the **Storage** property.</span></span>
<span data-ttu-id="cabc4-121">A parancs átadja azokat az értékeket, amelyek LocallyRedundant a Measure-Object parancsmagnak, amely megszámolja a találatokat.</span><span class="sxs-lookup"><span data-stu-id="cabc4-121">The command passes the ones that have a value of LocallyRedundant to the Measure-Object cmdlet, which counts the results.</span></span>
<span data-ttu-id="cabc4-122">További információért írja be a következőt: `Get-Help Measure-Object` .</span><span class="sxs-lookup"><span data-stu-id="cabc4-122">For more information, type `Get-Help Measure-Object`.</span></span>

## <span data-ttu-id="cabc4-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cabc4-123">PARAMETERS</span></span>

### <span data-ttu-id="cabc4-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cabc4-124">-Name</span></span>
<span data-ttu-id="cabc4-125">Itt adhatja meg annak a biztonságimásolat-tárolónak a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="cabc4-125">Specifies the name of the Backup vault that this cmdlet gets.</span></span>
<span data-ttu-id="cabc4-126">Ha egynél több biztonságimásolat-tárolóval rendelkezik, akkor ez a parancsmag mindet visszaadja.</span><span class="sxs-lookup"><span data-stu-id="cabc4-126">If more than one Backup vault has the same name, this cmdlet returns them all.</span></span>
<span data-ttu-id="cabc4-127">Adja meg a *ResourceGroupName* paramétert egy egyedi boltozat beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="cabc4-127">Specify the *ResourceGroupName* parameter to get a unique vault.</span></span>

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

### <span data-ttu-id="cabc4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cabc4-128">-ResourceGroupName</span></span>
<span data-ttu-id="cabc4-129">Annak az Azure-erőforrásnak a nevét adja meg, amelyben ez a parancsmag biztonsági mentési boltozatot kap.</span><span class="sxs-lookup"><span data-stu-id="cabc4-129">Specifies the name of an Azure resource group in which this cmdlet gets a Backup vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cabc4-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cabc4-130">-DefaultProfile</span></span>
<span data-ttu-id="cabc4-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cabc4-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cabc4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cabc4-132">CommonParameters</span></span>
<span data-ttu-id="cabc4-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cabc4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cabc4-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cabc4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cabc4-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cabc4-135">INPUTS</span></span>

## <span data-ttu-id="cabc4-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cabc4-136">OUTPUTS</span></span>

### <span data-ttu-id="cabc4-137">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="cabc4-137">AzureRmBackupVault</span></span>

## <span data-ttu-id="cabc4-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cabc4-138">NOTES</span></span>
* <span data-ttu-id="cabc4-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="cabc4-139">None</span></span>

## <span data-ttu-id="cabc4-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cabc4-140">RELATED LINKS</span></span>

[<span data-ttu-id="cabc4-141">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="cabc4-141">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="cabc4-142">Új – AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="cabc4-142">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="cabc4-143">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="cabc4-143">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="cabc4-144">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="cabc4-144">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


