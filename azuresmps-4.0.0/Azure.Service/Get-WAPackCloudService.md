---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4BAD0DDE-80D4-4A89-AFFB-78C933D2C0D5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76771d8c0e8d06cbe134e920a06be5fc1b109fe2
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017353"
---
# <span data-ttu-id="185e6-101">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="185e6-101">Get-WAPackCloudService</span></span>

## <span data-ttu-id="185e6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="185e6-102">SYNOPSIS</span></span>
<span data-ttu-id="185e6-103">Felhőbeli szolgáltatási objektumokat kap.</span><span class="sxs-lookup"><span data-stu-id="185e6-103">Gets cloud service objects.</span></span>

## <span data-ttu-id="185e6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="185e6-104">SYNTAX</span></span>

### <span data-ttu-id="185e6-105">Üres (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="185e6-105">Empty (Default)</span></span>
```
Get-WAPackCloudService [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="185e6-106">FromName</span><span class="sxs-lookup"><span data-stu-id="185e6-106">FromName</span></span>
```
Get-WAPackCloudService [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="185e6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="185e6-107">DESCRIPTION</span></span>
<span data-ttu-id="185e6-108">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="185e6-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="185e6-109">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="185e6-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="185e6-110">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="185e6-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="185e6-111">A **Get-WAPackCloudService** parancsmag Felhőbeli szolgáltatási objektumokat kap.</span><span class="sxs-lookup"><span data-stu-id="185e6-111">The **Get-WAPackCloudService** cmdlet gets cloud service objects.</span></span>

## <span data-ttu-id="185e6-112">Példák</span><span class="sxs-lookup"><span data-stu-id="185e6-112">EXAMPLES</span></span>

## <span data-ttu-id="185e6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="185e6-113">PARAMETERS</span></span>

### <span data-ttu-id="185e6-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="185e6-114">-Name</span></span>
<span data-ttu-id="185e6-115">Egy felhőalapú szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="185e6-115">Specifies the name of a cloud service.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="185e6-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="185e6-116">-Profile</span></span>
<span data-ttu-id="185e6-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="185e6-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="185e6-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="185e6-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="185e6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="185e6-119">CommonParameters</span></span>
<span data-ttu-id="185e6-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="185e6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="185e6-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="185e6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="185e6-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="185e6-122">INPUTS</span></span>

## <span data-ttu-id="185e6-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="185e6-123">OUTPUTS</span></span>

## <span data-ttu-id="185e6-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="185e6-124">NOTES</span></span>

## <span data-ttu-id="185e6-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="185e6-125">RELATED LINKS</span></span>

[<span data-ttu-id="185e6-126">Új – WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="185e6-126">New-WAPackCloudService</span></span>](./New-WAPackCloudService.md)

[<span data-ttu-id="185e6-127">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="185e6-127">Remove-WAPackCloudService</span></span>](./Remove-WAPackCloudService.md)


