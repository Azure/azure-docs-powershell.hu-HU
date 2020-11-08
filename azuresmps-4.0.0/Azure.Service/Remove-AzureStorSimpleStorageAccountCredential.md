---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 1BD296FB-8BFC-473F-951D-D2BF265E50AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 048be9276957ee865aa3204392b1dd847b0d6acf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016449"
---
# <span data-ttu-id="a31fd-101">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a31fd-101">Remove-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="a31fd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a31fd-102">SYNOPSIS</span></span>
<span data-ttu-id="a31fd-103">Törli a meglévő tárolási fiók hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="a31fd-103">Deletes an existing storage account credential.</span></span>

## <span data-ttu-id="a31fd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a31fd-104">SYNTAX</span></span>

### <span data-ttu-id="a31fd-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="a31fd-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a31fd-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="a31fd-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleStorageAccountCredential -SAC <StorageAccountCredentialResponse> [-WaitForComplete]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a31fd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a31fd-107">DESCRIPTION</span></span>
<span data-ttu-id="a31fd-108">A **Remove-AzureStorSimpleStorageAccountCredential** parancsmag törli a meglévő tárolási fiók hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="a31fd-108">The **Remove-AzureStorSimpleStorageAccountCredential** cmdlet deletes an existing storage account credential.</span></span>
<span data-ttu-id="a31fd-109">Adjon meg egy fiókot név szerint, vagy használja a **Get-AzureStorSimpleStorageAccountCredential** parancsmagot a törölni kívánt **StorageAccountCredential** -objektum beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="a31fd-109">Specify an account by name or use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet to obtain a **StorageAccountCredential** object to delete.</span></span>

## <span data-ttu-id="a31fd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a31fd-110">EXAMPLES</span></span>

### <span data-ttu-id="a31fd-111">1. példa: a tárolási fiók hitelesítő adatainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a31fd-111">Example 1: Remove a storage account credential</span></span>
```
PS C:\>Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" -Force
VERBOSE: ClientRequestId: 8e10d56b-ddb1-459b-b26e-a185f5a303de_PS
VERBOSE: About to create a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: 55cb6296-0156-4266-8591-d9e9bf8cc584_PS
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72 for tracking the task's status
```

<span data-ttu-id="a31fd-112">Ez a parancs eltávolítja a ContosoStorage07 nevű tárterület-fiókhoz tartozó hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="a31fd-112">This command removes the account credential for the storage account named ContosoStorage07.</span></span>
<span data-ttu-id="a31fd-113">Ez a parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="a31fd-113">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a31fd-114">A parancsmag a hitelesítő adatok megadását kérő üzenet nélkül távolítja el a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="a31fd-114">The cmdlet removes the credential without prompting your for confirmation.</span></span>

### <span data-ttu-id="a31fd-115">2. példa: a tárolási fiók hitelesítő adatainak eltávolítása a csővezeték-kezelő használatával</span><span class="sxs-lookup"><span data-stu-id="a31fd-115">Example 2: Remove a storage account credential by using the pipeline operator</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" | Remove-AzureStorSimpleStorageAccountCredential -Force -WaitForComplete
VERBOSE: ClientRequestId: f1b46216-bf4c-4c19-8e92-1dfe3894e258_PS
VERBOSE: ClientRequestId: 0d946f8f-c771-4ade-8a83-7c08dad86c52_PS
VERBOSE: ClientRequestId: 2000bab6-8311-4192-ad12-c67e35fc2697_PS
VERBOSE: Storage Access Credential with name ContosoStorage07 found! 
VERBOSE: About to run a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: b803b165-bef8-4a8f-9509-4b515ea8bdec_PS
VERBOSE: Your delete operation completed successfully!
```

<span data-ttu-id="a31fd-116">Ez a parancs a **Get-AzureStorSimpleStorageAccountCredential** parancsmaggal kapja meg a ContosoStorage07 nevű tárolási fiókot, majd átadja az adott objektumot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="a31fd-116">This command gets the storage account named ContosoStorage07 by using the **Get-AzureStorSimpleStorageAccountCredential** cmdlet, and then passes that object to the current cmdlet.</span></span>
<span data-ttu-id="a31fd-117">Az aktuális parancsmag eltávolítja az adott tárolási fiók hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="a31fd-117">The current cmdlet removes the credential for that storage account.</span></span>
<span data-ttu-id="a31fd-118">Ez a parancs a *WaitForComplete* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="a31fd-118">This command specifies the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="a31fd-119">A parancsmag nem adja vissza a vezérlőt addig, amíg el nem fejezi az eltávolítási műveletet.</span><span class="sxs-lookup"><span data-stu-id="a31fd-119">The cmdlet does not return control to the console until it completes the remove operation.</span></span>

## <span data-ttu-id="a31fd-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a31fd-120">PARAMETERS</span></span>

### <span data-ttu-id="a31fd-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a31fd-121">-Force</span></span>
<span data-ttu-id="a31fd-122">Azt jelzi, hogy ez a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a31fd-122">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a31fd-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="a31fd-123">-Profile</span></span>
<span data-ttu-id="a31fd-124">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="a31fd-124">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a31fd-125">-SAC</span><span class="sxs-lookup"><span data-stu-id="a31fd-125">-SAC</span></span>
<span data-ttu-id="a31fd-126">A hitelesítő adatokat **StorageAccountCredential** objektumként adja meg az eltávolításhoz.</span><span class="sxs-lookup"><span data-stu-id="a31fd-126">Specifies credential, as a **StorageAccountCredential** object, to remove.</span></span>
<span data-ttu-id="a31fd-127">Ha **StorageAccountCredential** objektumot szeretne beolvasni, használja a **Get-AzureStorSimpleStorageAccountCredential** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a31fd-127">To obtain a **StorageAccountCredential** object, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a31fd-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a31fd-128">-StorageAccountName</span></span>
<span data-ttu-id="a31fd-129">Annak a tárterület-fióknak a nevét adja meg, amelyet törölni szeretne.</span><span class="sxs-lookup"><span data-stu-id="a31fd-129">Specifies the name of the storage account credential to delete.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a31fd-130">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="a31fd-130">-WaitForComplete</span></span>
<span data-ttu-id="a31fd-131">Azt jelzi, hogy ez a parancsmag a művelet befejezését várja, mielőtt a vezérlőt visszaadja a Windows PowerShell-konzolnak.</span><span class="sxs-lookup"><span data-stu-id="a31fd-131">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a31fd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a31fd-132">CommonParameters</span></span>
<span data-ttu-id="a31fd-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a31fd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a31fd-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a31fd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a31fd-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a31fd-135">INPUTS</span></span>

### <span data-ttu-id="a31fd-136">StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a31fd-136">StorageAccountCredential</span></span>
<span data-ttu-id="a31fd-137">Ez a parancsmag a csővezeték segítségével fogadja el a **StorageAccountCredential** -objektumokat.</span><span class="sxs-lookup"><span data-stu-id="a31fd-137">This cmdlet accepts a **StorageAccountCredential** object by using the pipeline.</span></span>

## <span data-ttu-id="a31fd-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a31fd-138">OUTPUTS</span></span>

### <span data-ttu-id="a31fd-139">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="a31fd-139">TaskStatusInfo</span></span>
<span data-ttu-id="a31fd-140">Ez a parancsmag **TaskStatusInfo** -objektumot ad eredményül, ha a *WaitForComplete* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="a31fd-140">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="a31fd-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a31fd-141">NOTES</span></span>

## <span data-ttu-id="a31fd-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a31fd-142">RELATED LINKS</span></span>

[<span data-ttu-id="a31fd-143">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a31fd-143">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="a31fd-144">Új – AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a31fd-144">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="a31fd-145">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a31fd-145">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="a31fd-146">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="a31fd-146">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


