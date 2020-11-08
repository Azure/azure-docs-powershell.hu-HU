---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA2E37AB-F137-4A62-9ABC-90565305A23B
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6d1bbac3db6f69f5cdda14870de20eee7f8170b
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017357"
---
# <span data-ttu-id="e0da6-101">New-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="e0da6-101">New-WAPackCloudService</span></span>

## <span data-ttu-id="e0da6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0da6-102">SYNOPSIS</span></span>
<span data-ttu-id="e0da6-103">Felhőbeli szolgáltatást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e0da6-103">Creates a cloud service.</span></span>

## <span data-ttu-id="e0da6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0da6-104">SYNTAX</span></span>

```
New-WAPackCloudService -Name <String> -Label <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e0da6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0da6-105">DESCRIPTION</span></span>
<span data-ttu-id="e0da6-106">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="e0da6-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="e0da6-107">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="e0da6-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e0da6-108">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e0da6-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e0da6-109">A **New-WAPackCloudService** parancsmag létrehoz egy felhőalapú szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="e0da6-109">The **New-WAPackCloudService** cmdlet creates a cloud service.</span></span>

## <span data-ttu-id="e0da6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e0da6-110">EXAMPLES</span></span>

### <span data-ttu-id="e0da6-111">Példa 1: Felhőbeli szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="e0da6-111">Example 1: Create a cloud service</span></span>
```
PS C:\> New-WAPackCloudService -Name "ContosoCloudService01" -Label "A label"
```

<span data-ttu-id="e0da6-112">A parancs létrehoz egy ContosoCloudService01 nevű felhő-szolgáltatást a címkével.</span><span class="sxs-lookup"><span data-stu-id="e0da6-112">The command creates a cloud service named ContosoCloudService01 with a label.</span></span>

## <span data-ttu-id="e0da6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0da6-113">PARAMETERS</span></span>

### <span data-ttu-id="e0da6-114">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="e0da6-114">-Label</span></span>
<span data-ttu-id="e0da6-115">A felhőalapú szolgáltatás címkéjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0da6-115">Specifies a label for the cloud service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0da6-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e0da6-116">-Name</span></span>
<span data-ttu-id="e0da6-117">A cloudservice nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0da6-117">Specifies a name for the cloudservice.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0da6-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="e0da6-118">-Profile</span></span>
<span data-ttu-id="e0da6-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="e0da6-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e0da6-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="e0da6-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e0da6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0da6-121">CommonParameters</span></span>
<span data-ttu-id="e0da6-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0da6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0da6-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0da6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0da6-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0da6-124">INPUTS</span></span>

## <span data-ttu-id="e0da6-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0da6-125">OUTPUTS</span></span>

## <span data-ttu-id="e0da6-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0da6-126">NOTES</span></span>

## <span data-ttu-id="e0da6-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0da6-127">RELATED LINKS</span></span>

[<span data-ttu-id="e0da6-128">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="e0da6-128">Get-WAPackCloudService</span></span>](./Get-WAPackCloudService.md)

[<span data-ttu-id="e0da6-129">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="e0da6-129">Remove-WAPackCloudService</span></span>](./Remove-WAPackCloudService.md)


