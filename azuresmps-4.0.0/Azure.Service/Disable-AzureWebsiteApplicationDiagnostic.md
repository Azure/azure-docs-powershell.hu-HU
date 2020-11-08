---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3422EFD0-88DC-4DF0-868C-5C63C9FA95EF
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9aa78f34abf17c2aa5858697f492f76ee124d91
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015690"
---
# <span data-ttu-id="1ffb6-101">Disable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1ffb6-101">Disable-AzureWebsiteApplicationDiagnostic</span></span>

## <span data-ttu-id="1ffb6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ffb6-102">SYNOPSIS</span></span>
<span data-ttu-id="1ffb6-103">Az alkalmazás-diagnosztika letiltása Azure-webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="1ffb6-103">Disables application diagnostics for an Azure website.</span></span>

## <span data-ttu-id="1ffb6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ffb6-104">SYNTAX</span></span>

```
Disable-AzureWebsiteApplicationDiagnostic [-PassThru] [-File] [-TableStorage] [-BlobStorage] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1ffb6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ffb6-105">DESCRIPTION</span></span>
<span data-ttu-id="1ffb6-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="1ffb6-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1ffb6-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="1ffb6-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="1ffb6-108">Az alkalmazás-diagnosztika letiltása Azure-webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="1ffb6-108">Disables application diagnostics for an Azure website.</span></span>
<span data-ttu-id="1ffb6-109">Letiltja a naplózást a fájlrendszeren vagy az Azure-on tárolt naplózásban.</span><span class="sxs-lookup"><span data-stu-id="1ffb6-109">Disables logging configured to be stored on a file system or on Azure.</span></span>

## <span data-ttu-id="1ffb6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1ffb6-110">EXAMPLES</span></span>

### <span data-ttu-id="1ffb6-111">1. példa: az alkalmazás-naplózási fájl letiltása</span><span class="sxs-lookup"><span data-stu-id="1ffb6-111">Example 1:  Disable application logging file</span></span>
```
PS C:\> Disable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -File
```

<span data-ttu-id="1ffb6-112">Az alábbi példa letiltja az alkalmazások naplózását a fájlrendszerben.</span><span class="sxs-lookup"><span data-stu-id="1ffb6-112">The following example disables application logging on the file system.</span></span>

### <span data-ttu-id="1ffb6-113">2. példa: a naplózás letiltása az Azure Storage szolgáltatással</span><span class="sxs-lookup"><span data-stu-id="1ffb6-113">Example 2:  Disable logging using Azure storage</span></span>
```
PS C:\> Disable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -Storage
```

<span data-ttu-id="1ffb6-114">Az alábbi példa letiltja az alkalmazások naplózását a tárterület használatával.</span><span class="sxs-lookup"><span data-stu-id="1ffb6-114">The following example disables application logging using storage.</span></span>

## <span data-ttu-id="1ffb6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ffb6-115">PARAMETERS</span></span>

### <span data-ttu-id="1ffb6-116">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="1ffb6-116">-BlobStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ffb6-117">-Fájl</span><span class="sxs-lookup"><span data-stu-id="1ffb6-117">-File</span></span>
<span data-ttu-id="1ffb6-118">Itt adhatja meg, hogy a fájlrendszert szeretné-e használni a naplófájlok tárolásához.</span><span class="sxs-lookup"><span data-stu-id="1ffb6-118">Specifies that you want to use the file system to store the log files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ffb6-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1ffb6-119">-Name</span></span>
<span data-ttu-id="1ffb6-120">A webhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ffb6-120">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="1ffb6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ffb6-121">-PassThru</span></span>
<span data-ttu-id="1ffb6-122">Megjelölés a True (igaz) értékre a sikeres visszatéréshez.</span><span class="sxs-lookup"><span data-stu-id="1ffb6-122">Flag to return true if succeeded.</span></span>

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

### <span data-ttu-id="1ffb6-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="1ffb6-123">-Profile</span></span>
<span data-ttu-id="1ffb6-124">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="1ffb6-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1ffb6-125">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="1ffb6-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1ffb6-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="1ffb6-126">-Slot</span></span>
<span data-ttu-id="1ffb6-127">A bővítőhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ffb6-127">Specifies the name of slot.</span></span>

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

### <span data-ttu-id="1ffb6-128">-TableStorage</span><span class="sxs-lookup"><span data-stu-id="1ffb6-128">-TableStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ffb6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ffb6-129">CommonParameters</span></span>
<span data-ttu-id="1ffb6-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ffb6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ffb6-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ffb6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ffb6-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ffb6-132">INPUTS</span></span>

## <span data-ttu-id="1ffb6-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ffb6-133">OUTPUTS</span></span>

## <span data-ttu-id="1ffb6-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ffb6-134">NOTES</span></span>

## <span data-ttu-id="1ffb6-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ffb6-135">RELATED LINKS</span></span>

[<span data-ttu-id="1ffb6-136">Enable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1ffb6-136">Enable-AzureWebsiteApplicationDiagnostic</span></span>](./Enable-AzureWebsiteApplicationDiagnostic.md)

[<span data-ttu-id="1ffb6-137">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1ffb6-137">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="1ffb6-138">Új – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1ffb6-138">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="1ffb6-139">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1ffb6-139">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="1ffb6-140">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1ffb6-140">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


