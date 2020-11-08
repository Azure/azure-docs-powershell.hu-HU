---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BFB57100-93F6-4FD2-8ECA-7F54BEB0D6B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7114f39ee2b105c80429151df8347b5c17dcfea0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016506"
---
# <span data-ttu-id="6c5a1-101">Get-AzureWebsiteLog</span><span class="sxs-lookup"><span data-stu-id="6c5a1-101">Get-AzureWebsiteLog</span></span>

## <span data-ttu-id="6c5a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6c5a1-102">SYNOPSIS</span></span>
<span data-ttu-id="6c5a1-103">A megadott webhelyhez naplók jelentkeznek.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-103">Gets logs for the specified website.</span></span>

## <span data-ttu-id="6c5a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6c5a1-104">SYNTAX</span></span>

### <span data-ttu-id="6c5a1-105">Farok</span><span class="sxs-lookup"><span data-stu-id="6c5a1-105">Tail</span></span>
```
Get-AzureWebsiteLog [-Path <String>] [-Message <String>] [-Tail] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6c5a1-106">ListPath</span><span class="sxs-lookup"><span data-stu-id="6c5a1-106">ListPath</span></span>
```
Get-AzureWebsiteLog [-ListPath] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c5a1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6c5a1-107">DESCRIPTION</span></span>
<span data-ttu-id="6c5a1-108">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6c5a1-109">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6c5a1-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6c5a1-110">A megadott webhely naplózása.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-110">Gets log for the specified website.</span></span>

## <span data-ttu-id="6c5a1-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6c5a1-111">EXAMPLES</span></span>

### <span data-ttu-id="6c5a1-112">Példa 1: a napló folyamatos indítása</span><span class="sxs-lookup"><span data-stu-id="6c5a1-112">Example 1: Start log streaming</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail
```

<span data-ttu-id="6c5a1-113">Ez a példa elindítja a naplózást az összes alkalmazás-naplóban.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-113">This example starts log streaming for all application logs.</span></span>

### <span data-ttu-id="6c5a1-114">2. példa: naplók indítása a http-naplókból</span><span class="sxs-lookup"><span data-stu-id="6c5a1-114">Example 2: Start log streaming for http logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail -Path http
```

<span data-ttu-id="6c5a1-115">Ez a példa elindítja a http-naplók naplózását.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-115">This example starts log streaming for http logs.</span></span>

### <span data-ttu-id="6c5a1-116">3. példa: naplók indítása a hibanapló továbbításához</span><span class="sxs-lookup"><span data-stu-id="6c5a1-116">Example 3: Start log streaming for error logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail -Message Error
```

<span data-ttu-id="6c5a1-117">Ez a példa elindítja a naplózási adatfolyamot, és csak a hibák naplózását jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-117">This example starts log streaming and show error logs only.</span></span>

### <span data-ttu-id="6c5a1-118">4. példa: avaiable naplók megjelenítése</span><span class="sxs-lookup"><span data-stu-id="6c5a1-118">Example 4: Display avaiable logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Name MyWebsite -ListPath
```

<span data-ttu-id="6c5a1-119">Ez a példa felsorolja a webhely összes elérhető naplózási útvonalát.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-119">This example lists all available log paths in the website.</span></span>

## <span data-ttu-id="6c5a1-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6c5a1-120">PARAMETERS</span></span>

### <span data-ttu-id="6c5a1-121">-ListPath</span><span class="sxs-lookup"><span data-stu-id="6c5a1-121">-ListPath</span></span>
<span data-ttu-id="6c5a1-122">Azt jelzi, hogy a napló elérési útvonalait szeretné-e listázni</span><span class="sxs-lookup"><span data-stu-id="6c5a1-122">Indicates whether to list the log paths.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListPath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c5a1-123">-Üzenet</span><span class="sxs-lookup"><span data-stu-id="6c5a1-123">-Message</span></span>
<span data-ttu-id="6c5a1-124">Itt adhatja meg azt a karakterláncot, amelyet a rendszer a napló üzenetének szűréséhez fog használni.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-124">Specifies a string which will be used to filter the log message.</span></span>
<span data-ttu-id="6c5a1-125">Csak a karakterláncot tartalmazó naplók lesznek beolvasva.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-125">Only logs which contains this string will be retrieved.</span></span>

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c5a1-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6c5a1-126">-Name</span></span>
<span data-ttu-id="6c5a1-127">A webhely neve.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-127">The name of the website.</span></span>

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

### <span data-ttu-id="6c5a1-128">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="6c5a1-128">-Path</span></span>
<span data-ttu-id="6c5a1-129">Az az útvonal, amelyből a naplót vissza kívánja olvasni.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-129">The path from which the log will be retrieved.</span></span>
<span data-ttu-id="6c5a1-130">Alapértelmezés szerint ez a root, ami azt jelenti, hogy az összes elérési utat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-130">By default it is Root, which means include all the paths.</span></span>

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c5a1-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="6c5a1-131">-Profile</span></span>
<span data-ttu-id="6c5a1-132">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6c5a1-133">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6c5a1-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="6c5a1-134">-Slot</span></span>
<span data-ttu-id="6c5a1-135">A bővítőhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-135">Specifies the slot name.</span></span>

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

### <span data-ttu-id="6c5a1-136">-Farok</span><span class="sxs-lookup"><span data-stu-id="6c5a1-136">-Tail</span></span>
<span data-ttu-id="6c5a1-137">Itt adhatja meg, hogy a naplókat szeretné-e továbbítani.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-137">Specifies whether to stream the logs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Tail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c5a1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c5a1-138">CommonParameters</span></span>
<span data-ttu-id="6c5a1-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6c5a1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c5a1-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c5a1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c5a1-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c5a1-141">INPUTS</span></span>

## <span data-ttu-id="6c5a1-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c5a1-142">OUTPUTS</span></span>

## <span data-ttu-id="6c5a1-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6c5a1-143">NOTES</span></span>

## <span data-ttu-id="6c5a1-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c5a1-144">RELATED LINKS</span></span>

[<span data-ttu-id="6c5a1-145">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6c5a1-145">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="6c5a1-146">Új – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6c5a1-146">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="6c5a1-147">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6c5a1-147">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="6c5a1-148">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6c5a1-148">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


