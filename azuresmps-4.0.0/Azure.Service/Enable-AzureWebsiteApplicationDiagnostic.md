---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 99A03E14-254E-4E72-8EA9-2FE2A5CEA597
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58e7cafb1fe774abcaf2290168b8254562bad89b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015682"
---
# <span data-ttu-id="e894a-101">Enable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e894a-101">Enable-AzureWebsiteApplicationDiagnostic</span></span>

## <span data-ttu-id="e894a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e894a-102">SYNOPSIS</span></span>
<span data-ttu-id="e894a-103">Engedélyezi az alkalmazás-diagnosztikát az Azure-webhelyeken.</span><span class="sxs-lookup"><span data-stu-id="e894a-103">Enables application diagnostics on an Azure website.</span></span>

## <span data-ttu-id="e894a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e894a-104">SYNTAX</span></span>

### <span data-ttu-id="e894a-105">FileParameterSet</span><span class="sxs-lookup"><span data-stu-id="e894a-105">FileParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-File] -LogLevel <LogEntryType> [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e894a-106">TableStorageParameterSet</span><span class="sxs-lookup"><span data-stu-id="e894a-106">TableStorageParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-TableStorage] -LogLevel <LogEntryType>
 [-StorageAccountName <String>] [-StorageTableName <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e894a-107">BlobStorageParameterSet</span><span class="sxs-lookup"><span data-stu-id="e894a-107">BlobStorageParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-BlobStorage] -LogLevel <LogEntryType>
 [-StorageAccountName <String>] [-StorageBlobContainerName <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e894a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e894a-108">DESCRIPTION</span></span>
<span data-ttu-id="e894a-109">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="e894a-109">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e894a-110">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e894a-110">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e894a-111">Engedélyezi az alkalmazások diagnosztikai szolgáltatását egy Azure-webhelyen, és lehetővé teszi a naplófájlok tárolását a fájlrendszerben vagy az Azure-tárterületen.</span><span class="sxs-lookup"><span data-stu-id="e894a-111">Enables application diagnostics on an Azure website, and allows you to configure storage of logs on a file system or on Azure storage.</span></span>

## <span data-ttu-id="e894a-112">Példák</span><span class="sxs-lookup"><span data-stu-id="e894a-112">EXAMPLES</span></span>

### <span data-ttu-id="e894a-113">1. példa: a diagnosztika engedélyezése a fájlrendszer használatával</span><span class="sxs-lookup"><span data-stu-id="e894a-113">Example 1: Enable diagnostics using file system</span></span>
```
PS C:\> Enable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -File -LogLevel Verbose
```

<span data-ttu-id="e894a-114">Ez a példa lehetővé teszi az alkalmazások naplózását a fájlrendszerben bőbeszédű szintre.</span><span class="sxs-lookup"><span data-stu-id="e894a-114">This example enables application logging on file system with verbose level.</span></span>

### <span data-ttu-id="e894a-115">2. példa: a naplózás engedélyezése az Azure Storage szolgáltatással</span><span class="sxs-lookup"><span data-stu-id="e894a-115">Example 2: Enable logging using Azure Storage</span></span>
```
PS C:\> Enable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -Storage -LogLevel Information -StorageAccountName myaccount
```

<span data-ttu-id="e894a-116">Ez a példa lehetővé teszi az alkalmazások naplózását a MyAccount nevű tárterület-fiókkal az adatok naplózási szinttel beállításával.</span><span class="sxs-lookup"><span data-stu-id="e894a-116">This example enables application logging using storage account named myaccount with logging level set to Information.</span></span>

## <span data-ttu-id="e894a-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e894a-117">PARAMETERS</span></span>

### <span data-ttu-id="e894a-118">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="e894a-118">-BlobStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: BlobStorageParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e894a-119">-Fájl</span><span class="sxs-lookup"><span data-stu-id="e894a-119">-File</span></span>
<span data-ttu-id="e894a-120">Itt adhatja meg, hogy a naplófájlokat a fájlrendszerrel szeretné-e menteni.</span><span class="sxs-lookup"><span data-stu-id="e894a-120">Specifies that you want to use a file system to store the log files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FileParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e894a-121">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="e894a-121">-LogLevel</span></span>
<span data-ttu-id="e894a-122">A tárolandó napló szintje.</span><span class="sxs-lookup"><span data-stu-id="e894a-122">The log level to store.</span></span>
<span data-ttu-id="e894a-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e894a-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e894a-124">Hiba</span><span class="sxs-lookup"><span data-stu-id="e894a-124">Error</span></span>
- <span data-ttu-id="e894a-125">Figyelmeztetés</span><span class="sxs-lookup"><span data-stu-id="e894a-125">Warning</span></span>
- <span data-ttu-id="e894a-126">Információk</span><span class="sxs-lookup"><span data-stu-id="e894a-126">Information</span></span>
- <span data-ttu-id="e894a-127">Részletes</span><span class="sxs-lookup"><span data-stu-id="e894a-127">Verbose</span></span>

```yaml
Type: LogEntryType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e894a-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e894a-128">-Name</span></span>
<span data-ttu-id="e894a-129">Az Azure-webhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e894a-129">Specifies the name of the Azure website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e894a-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e894a-130">-PassThru</span></span>
<span data-ttu-id="e894a-131">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="e894a-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e894a-132">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="e894a-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e894a-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="e894a-133">-Profile</span></span>
<span data-ttu-id="e894a-134">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="e894a-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e894a-135">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="e894a-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e894a-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="e894a-136">-Slot</span></span>
<span data-ttu-id="e894a-137">A bővítőhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e894a-137">Specifies the name of the slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e894a-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e894a-138">-StorageAccountName</span></span>
<span data-ttu-id="e894a-139">A naplók tárolásához használandó tárolási fiók.</span><span class="sxs-lookup"><span data-stu-id="e894a-139">The storage account to use for storing the logs.</span></span>
<span data-ttu-id="e894a-140">Ha nincs megadva, a program a CurrentStorageAccount használja.</span><span class="sxs-lookup"><span data-stu-id="e894a-140">If not specified, the CurrentStorageAccount is used.</span></span>

```yaml
Type: String
Parameter Sets: TableStorageParameterSet, BlobStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e894a-141">-StorageBlobContainerName</span><span class="sxs-lookup"><span data-stu-id="e894a-141">-StorageBlobContainerName</span></span>
```yaml
Type: String
Parameter Sets: BlobStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e894a-142">-StorageTableName</span><span class="sxs-lookup"><span data-stu-id="e894a-142">-StorageTableName</span></span>
```yaml
Type: String
Parameter Sets: TableStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e894a-143">-TableStorage</span><span class="sxs-lookup"><span data-stu-id="e894a-143">-TableStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: TableStorageParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e894a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e894a-144">CommonParameters</span></span>
<span data-ttu-id="e894a-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e894a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e894a-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e894a-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e894a-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e894a-147">INPUTS</span></span>

## <span data-ttu-id="e894a-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e894a-148">OUTPUTS</span></span>

## <span data-ttu-id="e894a-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e894a-149">NOTES</span></span>

## <span data-ttu-id="e894a-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e894a-150">RELATED LINKS</span></span>

[<span data-ttu-id="e894a-151">Disable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e894a-151">Disable-AzureWebsiteApplicationDiagnostic</span></span>](./Disable-AzureWebsiteApplicationDiagnostic.md)

[<span data-ttu-id="e894a-152">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e894a-152">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="e894a-153">Új – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e894a-153">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="e894a-154">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e894a-154">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="e894a-155">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e894a-155">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


