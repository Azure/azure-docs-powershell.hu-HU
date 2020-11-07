---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: 18383ffeb35b1ce6bb2651be041e07b6164e55da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680202"
---
# <span data-ttu-id="b1b94-101">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b1b94-101">Get-AzureRmBackupVault</span></span>

## <span data-ttu-id="b1b94-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b1b94-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b94-103">Biztonsági mentési boltozatokat kap.</span><span class="sxs-lookup"><span data-stu-id="b1b94-103">Gets Backup vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1b94-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b1b94-104">SYNTAX</span></span>

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1b94-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b1b94-105">DESCRIPTION</span></span>
<span data-ttu-id="b1b94-106">A **Get-AzureRmBackupVault** parancsmag Azure Backup-boltozatokat kap.</span><span class="sxs-lookup"><span data-stu-id="b1b94-106">The **Get-AzureRmBackupVault** cmdlet gets Azure Backup vaults.</span></span>
<span data-ttu-id="b1b94-107">Ez a parancsmag a más parancsmagokkal használható **AzureRmBackupVault** -objektumokat számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b1b94-107">This cmdlet returns **AzureRmBackupVault** objects for use with other cmdlets.</span></span>

## <span data-ttu-id="b1b94-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b1b94-108">EXAMPLES</span></span>

### <span data-ttu-id="b1b94-109">Példa 1: az összes biztonságimásolat-boltozat megtekintése</span><span class="sxs-lookup"><span data-stu-id="b1b94-109">Example 1: View all the Backup vaults</span></span>
```
PS C:\>Get-AzureRmBackupVault
```

<span data-ttu-id="b1b94-110">Ez a parancs minden Azure biztonságimásolat-tárolót kap.</span><span class="sxs-lookup"><span data-stu-id="b1b94-110">This command gets all the Azure Backup vaults.</span></span>

### <span data-ttu-id="b1b94-111">2. példa: a West US-ban létrehozott összes boltozat megtekintése</span><span class="sxs-lookup"><span data-stu-id="b1b94-111">Example 2: View all vaults created in West US</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

<span data-ttu-id="b1b94-112">Ez a parancs a biztonságimásolat-tárolókat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b1b94-112">This command gets all the Backup vaults.</span></span>
<span data-ttu-id="b1b94-113">A parancs a csővezeték-kezelő segítségével átadja őket a Where-Object parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="b1b94-113">The command passes them to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b1b94-114">Az adott parancsmag a **régió** tulajdonság alapján szűri az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="b1b94-114">That cmdlet filters the results based on the **Region** property.</span></span>
<span data-ttu-id="b1b94-115">További információért írja be a következőt: `Get-Help Where-Object` .</span><span class="sxs-lookup"><span data-stu-id="b1b94-115">For more information, type `Get-Help Where-Object`.</span></span>

### <span data-ttu-id="b1b94-116">3. példa: speciális boltozat beszerzése</span><span class="sxs-lookup"><span data-stu-id="b1b94-116">Example 3: Get a specific vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="b1b94-117">Ez a parancs a Vault03 nevű boltozatot kapja.</span><span class="sxs-lookup"><span data-stu-id="b1b94-117">This command gets the vault named Vault03.</span></span>

### <span data-ttu-id="b1b94-118">Példa 4: a helyileg redundáns tárterületet tartalmazó boltozatok számának megszámolása</span><span class="sxs-lookup"><span data-stu-id="b1b94-118">Example 4: Count the number of vaults that have locally redundant storage</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

<span data-ttu-id="b1b94-119">Ez a parancs minden Azure biztonságimásolat-tárolót kap.</span><span class="sxs-lookup"><span data-stu-id="b1b94-119">This command gets all the Azure Backup vaults.</span></span>
<span data-ttu-id="b1b94-120">A parancs átadja azokat a **Where-Object** értékre, amely a **tárolási** tulajdonság alapján szűri az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="b1b94-120">The command passes them to **Where-Object** , which filters the results based on the **Storage** property.</span></span>
<span data-ttu-id="b1b94-121">A parancs átadja azokat az értékeket, amelyek LocallyRedundant a Measure-Object parancsmagnak, amely megszámolja a találatokat.</span><span class="sxs-lookup"><span data-stu-id="b1b94-121">The command passes the ones that have a value of LocallyRedundant to the Measure-Object cmdlet, which counts the results.</span></span>
<span data-ttu-id="b1b94-122">További információért írja be a következőt: `Get-Help Measure-Object` .</span><span class="sxs-lookup"><span data-stu-id="b1b94-122">For more information, type `Get-Help Measure-Object`.</span></span>

## <span data-ttu-id="b1b94-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b1b94-123">PARAMETERS</span></span>

### <span data-ttu-id="b1b94-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1b94-124">-DefaultProfile</span></span>
<span data-ttu-id="b1b94-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b1b94-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1b94-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b1b94-126">-Name</span></span>
<span data-ttu-id="b1b94-127">Itt adhatja meg annak a biztonságimásolat-tárolónak a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="b1b94-127">Specifies the name of the Backup vault that this cmdlet gets.</span></span>
<span data-ttu-id="b1b94-128">Ha egynél több biztonságimásolat-tárolóval rendelkezik, akkor ez a parancsmag mindet visszaadja.</span><span class="sxs-lookup"><span data-stu-id="b1b94-128">If more than one Backup vault has the same name, this cmdlet returns them all.</span></span>
<span data-ttu-id="b1b94-129">Adja meg a *ResourceGroupName* paramétert egy egyedi boltozat beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="b1b94-129">Specify the *ResourceGroupName* parameter to get a unique vault.</span></span>

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

### <span data-ttu-id="b1b94-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1b94-130">-ResourceGroupName</span></span>
<span data-ttu-id="b1b94-131">Annak az Azure-erőforrásnak a nevét adja meg, amelyben ez a parancsmag biztonsági mentési boltozatot kap.</span><span class="sxs-lookup"><span data-stu-id="b1b94-131">Specifies the name of an Azure resource group in which this cmdlet gets a Backup vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b94-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b94-132">CommonParameters</span></span>
<span data-ttu-id="b1b94-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b1b94-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b94-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1b94-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b94-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1b94-135">INPUTS</span></span>

### <span data-ttu-id="b1b94-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="b1b94-136">None</span></span>
<span data-ttu-id="b1b94-137">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b1b94-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b1b94-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1b94-138">OUTPUTS</span></span>

### <span data-ttu-id="b1b94-139">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b1b94-139">AzureRmBackupVault</span></span>

## <span data-ttu-id="b1b94-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b1b94-140">NOTES</span></span>
* <span data-ttu-id="b1b94-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="b1b94-141">None</span></span>

## <span data-ttu-id="b1b94-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1b94-142">RELATED LINKS</span></span>

[<span data-ttu-id="b1b94-143">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b1b94-143">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="b1b94-144">Új – AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b1b94-144">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="b1b94-145">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b1b94-145">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="b1b94-146">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b1b94-146">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


