---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 947D1C09-7CFA-4E97-A6B3-2DA9D7507F0C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0260b452c96b5f6dd60599b5da15cc323b5423d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016263"
---
# <span data-ttu-id="49899-101">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="49899-101">Get-WAPackVNet</span></span>

## <span data-ttu-id="49899-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="49899-102">SYNOPSIS</span></span>
<span data-ttu-id="49899-103">Virtuális hálózatokat kap.</span><span class="sxs-lookup"><span data-stu-id="49899-103">Gets virtual networks.</span></span>

## <span data-ttu-id="49899-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="49899-104">SYNTAX</span></span>

### <span data-ttu-id="49899-105">Üres (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="49899-105">Empty (Default)</span></span>
```
Get-WAPackVNet [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="49899-106">FromId</span><span class="sxs-lookup"><span data-stu-id="49899-106">FromId</span></span>
```
Get-WAPackVNet -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="49899-107">FromName</span><span class="sxs-lookup"><span data-stu-id="49899-107">FromName</span></span>
```
Get-WAPackVNet -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="49899-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="49899-108">DESCRIPTION</span></span>
<span data-ttu-id="49899-109">A **Get-WAPackVNet** parancsmag virtuális hálózatokat kap.</span><span class="sxs-lookup"><span data-stu-id="49899-109">The **Get-WAPackVNet** cmdlet gets virtual networks.</span></span>

## <span data-ttu-id="49899-110">Példák</span><span class="sxs-lookup"><span data-stu-id="49899-110">EXAMPLES</span></span>

### <span data-ttu-id="49899-111">Példa 1: az összes virtuális hálózat beszerzése</span><span class="sxs-lookup"><span data-stu-id="49899-111">Example 1: Get all virtual networks</span></span>
```
PS C:\> Get-WAPackVNet
```

<span data-ttu-id="49899-112">Ez a parancs a virtuális hálózatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="49899-112">This command gets all virtual networks.</span></span>

### <span data-ttu-id="49899-113">2. példa: virtuális hálózat beszerzése azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="49899-113">Example 2: Get a virtual network by using an ID</span></span>
```
PS C:\> Get-WAPackVNet -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="49899-114">Ez a parancs a megadott azonosítót tartalmazó virtuális hálózatot kapja.</span><span class="sxs-lookup"><span data-stu-id="49899-114">This command gets the virtual network that has the specified ID.</span></span>

### <span data-ttu-id="49899-115">3. példa: virtuális hálózat beszerzése név használatával</span><span class="sxs-lookup"><span data-stu-id="49899-115">Example 3: Get a virtual network by using a name</span></span>
```
PS C:\> Get-WAPackVNet -Name "ContosoVNet08"
```

<span data-ttu-id="49899-116">Ez a parancs a ContosoVNet08 nevű virtuális hálózatot kapja.</span><span class="sxs-lookup"><span data-stu-id="49899-116">This command gets the virtual network named ContosoVNet08.</span></span>

## <span data-ttu-id="49899-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="49899-117">PARAMETERS</span></span>

### <span data-ttu-id="49899-118">-AZONOSÍTÓ</span><span class="sxs-lookup"><span data-stu-id="49899-118">-ID</span></span>
<span data-ttu-id="49899-119">A virtuális hálózat egyedi AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="49899-119">Specifies the unique ID of a virtual network.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49899-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="49899-120">-Name</span></span>
<span data-ttu-id="49899-121">A virtuális hálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49899-121">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49899-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="49899-122">-Profile</span></span>
<span data-ttu-id="49899-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="49899-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="49899-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="49899-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="49899-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49899-125">CommonParameters</span></span>
<span data-ttu-id="49899-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="49899-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49899-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49899-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49899-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="49899-128">INPUTS</span></span>

## <span data-ttu-id="49899-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49899-129">OUTPUTS</span></span>

## <span data-ttu-id="49899-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="49899-130">NOTES</span></span>

## <span data-ttu-id="49899-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49899-131">RELATED LINKS</span></span>

