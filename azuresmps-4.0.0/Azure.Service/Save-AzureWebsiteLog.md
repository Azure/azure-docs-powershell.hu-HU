---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4696BB05-F507-4FFB-8D96-6BAA2EBB0F0A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 03acdfb16c7f1e7e8ee5e6b95902ef1ed056412a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015458"
---
# <span data-ttu-id="3a704-101">Save-AzureWebsiteLog</span><span class="sxs-lookup"><span data-stu-id="3a704-101">Save-AzureWebsiteLog</span></span>

## <span data-ttu-id="3a704-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a704-102">SYNOPSIS</span></span>
<span data-ttu-id="3a704-103">Letölti és menti a naplókat a megadott webhelyre.</span><span class="sxs-lookup"><span data-stu-id="3a704-103">Downloads and saves the logs for a specified website.</span></span>

## <span data-ttu-id="3a704-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a704-104">SYNTAX</span></span>

```
Save-AzureWebsiteLog [-Output <String>] [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3a704-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a704-105">DESCRIPTION</span></span>
<span data-ttu-id="3a704-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="3a704-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3a704-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3a704-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3a704-108">A **Save-AzureWebsiteLog** parancsmag letölti a megadott webhely naplóit.</span><span class="sxs-lookup"><span data-stu-id="3a704-108">The **Save-AzureWebsiteLog** cmdlet downloads the logs for a specified website.</span></span>

## <span data-ttu-id="3a704-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3a704-109">EXAMPLES</span></span>

### <span data-ttu-id="3a704-110">Példa 1: webhelyre vonatkozó naplók letöltése és mentése</span><span class="sxs-lookup"><span data-stu-id="3a704-110">Example 1: Download and save logs for a website</span></span>
```
PS C:\> Save-AzureWebsiteLogs -Name mySite -Output .\logs.zip
```

<span data-ttu-id="3a704-111">Ez a példa letölti a webhelyek mySite a futásidejű és a központi üzembe állítási naplókat a fájl logs.zip az aktuális címtárban.</span><span class="sxs-lookup"><span data-stu-id="3a704-111">This example downloads the runtime and deployment logs for website mySite to the file logs.zip in the current directory.</span></span>

## <span data-ttu-id="3a704-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a704-112">PARAMETERS</span></span>

### <span data-ttu-id="3a704-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3a704-113">-Name</span></span>
<span data-ttu-id="3a704-114">A webhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a704-114">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="3a704-115">-Output (kimenet)</span><span class="sxs-lookup"><span data-stu-id="3a704-115">-Output</span></span>
<span data-ttu-id="3a704-116">A letöltött fájl tárolási elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a704-116">Specifies the path to store the downloaded file.</span></span>

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

### <span data-ttu-id="3a704-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a704-117">-PassThru</span></span>
<span data-ttu-id="3a704-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="3a704-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3a704-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="3a704-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a704-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="3a704-120">-Profile</span></span>
<span data-ttu-id="3a704-121">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3a704-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3a704-122">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3a704-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3a704-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="3a704-123">-Slot</span></span>
<span data-ttu-id="3a704-124">A bővítőhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a704-124">Specifies the slot name.</span></span>

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

### <span data-ttu-id="3a704-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a704-125">CommonParameters</span></span>
<span data-ttu-id="3a704-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a704-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a704-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a704-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a704-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a704-128">INPUTS</span></span>

## <span data-ttu-id="3a704-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a704-129">OUTPUTS</span></span>

## <span data-ttu-id="3a704-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a704-130">NOTES</span></span>

## <span data-ttu-id="3a704-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a704-131">RELATED LINKS</span></span>

[<span data-ttu-id="3a704-132">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="3a704-132">Restore-AzureWebsiteDeployment</span></span>](./Restore-AzureWebsiteDeployment.md)


