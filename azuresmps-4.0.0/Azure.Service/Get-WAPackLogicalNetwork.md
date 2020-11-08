---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7D51BE56-C0A2-4A32-BB7F-8FA9CC67F8F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 986d4998119c4ede1780fa35ad6baadce4574a81
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017354"
---
# <span data-ttu-id="7da92-101">Get-WAPackLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="7da92-101">Get-WAPackLogicalNetwork</span></span>

## <span data-ttu-id="7da92-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7da92-102">SYNOPSIS</span></span>
<span data-ttu-id="7da92-103">Logikai hálózati objektumok jelentkeznek.</span><span class="sxs-lookup"><span data-stu-id="7da92-103">Gets logical network objects.</span></span>

## <span data-ttu-id="7da92-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7da92-104">SYNTAX</span></span>

### <span data-ttu-id="7da92-105">Üres (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7da92-105">Empty (Default)</span></span>
```
Get-WAPackLogicalNetwork [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7da92-106">FromName</span><span class="sxs-lookup"><span data-stu-id="7da92-106">FromName</span></span>
```
Get-WAPackLogicalNetwork [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7da92-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7da92-107">DESCRIPTION</span></span>
<span data-ttu-id="7da92-108">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="7da92-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="7da92-109">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="7da92-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7da92-110">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7da92-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7da92-111">A **Get-WAPackLogicalNetwork** parancsmag logikai hálózati objektumokat kap.</span><span class="sxs-lookup"><span data-stu-id="7da92-111">The **Get-WAPackLogicalNetwork** cmdlet gets logical network objects.</span></span>

## <span data-ttu-id="7da92-112">Példák</span><span class="sxs-lookup"><span data-stu-id="7da92-112">EXAMPLES</span></span>

### <span data-ttu-id="7da92-113">Példa 1: logikai hálózat beszerzése név használatával</span><span class="sxs-lookup"><span data-stu-id="7da92-113">Example 1: Get a logical network by using a name</span></span>
```
PS C:\> Get-WAPackLogicalNetwork -Name "ContosoLogicalNetwork01"
```

<span data-ttu-id="7da92-114">Ez a parancs a ContosoLogicalNetwork01 nevű logikai hálózatot kap.</span><span class="sxs-lookup"><span data-stu-id="7da92-114">This command gets a logical network named ContosoLogicalNetwork01.</span></span>

### <span data-ttu-id="7da92-115">2. példa: az összes logikai hálózat beolvasása</span><span class="sxs-lookup"><span data-stu-id="7da92-115">Example 2: Get all logical networks</span></span>
```
PS C:\> Get-WAPackLogicalNetwork
```

<span data-ttu-id="7da92-116">Ez a parancs a logikai hálózatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="7da92-116">This command gets all logical networks.</span></span>

## <span data-ttu-id="7da92-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7da92-117">PARAMETERS</span></span>

### <span data-ttu-id="7da92-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7da92-118">-Name</span></span>
<span data-ttu-id="7da92-119">A logikai hálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7da92-119">Specifies the name of a logical network.</span></span>

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

### <span data-ttu-id="7da92-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="7da92-120">-Profile</span></span>
<span data-ttu-id="7da92-121">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="7da92-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7da92-122">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="7da92-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7da92-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da92-123">CommonParameters</span></span>
<span data-ttu-id="7da92-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7da92-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da92-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7da92-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da92-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7da92-126">INPUTS</span></span>

## <span data-ttu-id="7da92-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7da92-127">OUTPUTS</span></span>

## <span data-ttu-id="7da92-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7da92-128">NOTES</span></span>

## <span data-ttu-id="7da92-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7da92-129">RELATED LINKS</span></span>

