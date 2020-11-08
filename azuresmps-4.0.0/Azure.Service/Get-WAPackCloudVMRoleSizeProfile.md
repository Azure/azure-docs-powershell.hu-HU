---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 453AEA42-E29C-4FF2-9210-0DD88B77DC07
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29c7f8bc814ddf5295064d89eeaf34c8e7274916
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016508"
---
# <span data-ttu-id="777c0-101">Get-WAPackCloudVMRoleSizeProfile</span><span class="sxs-lookup"><span data-stu-id="777c0-101">Get-WAPackCloudVMRoleSizeProfile</span></span>

## <span data-ttu-id="777c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="777c0-102">SYNOPSIS</span></span>
<span data-ttu-id="777c0-103">Cloud VM-szerepkörök méretének lekérdezési objektumait kapja.</span><span class="sxs-lookup"><span data-stu-id="777c0-103">Gets Cloud VM Role Size profile objects.</span></span>

## <span data-ttu-id="777c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="777c0-104">SYNTAX</span></span>

### <span data-ttu-id="777c0-105">Üres (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="777c0-105">Empty (Default)</span></span>
```
Get-WAPackCloudVMRoleSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="777c0-106">FromName</span><span class="sxs-lookup"><span data-stu-id="777c0-106">FromName</span></span>
```
Get-WAPackCloudVMRoleSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="777c0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="777c0-107">DESCRIPTION</span></span>
<span data-ttu-id="777c0-108">A **Get-WAPackCloudVMRoleSizeProfile** parancsmag a virtuális gépek felhőalapú VM-beli szerepkör-profil objektumait kapja.</span><span class="sxs-lookup"><span data-stu-id="777c0-108">The **Get-WAPackCloudVMRoleSizeProfile** cmdlet gets Cloud VM Role size profile objects for virtual machines.</span></span>

## <span data-ttu-id="777c0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="777c0-109">EXAMPLES</span></span>

### <span data-ttu-id="777c0-110">Példa 1: felhőalapú VM-beli szerepkör-méret profiljának beszerzése név használatával</span><span class="sxs-lookup"><span data-stu-id="777c0-110">Example 1: Get a Cloud VM Role size profile by using a name</span></span>
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile -Name "Small"
```

<span data-ttu-id="777c0-111">Ez a parancs a Small nevű méret profilt kapja.</span><span class="sxs-lookup"><span data-stu-id="777c0-111">This command gets the size profile named Small.</span></span>

### <span data-ttu-id="777c0-112">2. példa: a felhőalapú VM-szerepkörök méret-profiljainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="777c0-112">Example 2: Get all Cloud VM Role size profiles</span></span>
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile
```

<span data-ttu-id="777c0-113">Ez a parancs a teljes méretű profilokat kapja.</span><span class="sxs-lookup"><span data-stu-id="777c0-113">This command gets all the size profiles.</span></span>

## <span data-ttu-id="777c0-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="777c0-114">PARAMETERS</span></span>

### <span data-ttu-id="777c0-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="777c0-115">-Name</span></span>
<span data-ttu-id="777c0-116">A Felhőbeli VM-szerepkörök méretére vonatkozó profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="777c0-116">Specifies the name of a Cloud VM Role size profile.</span></span>

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

### <span data-ttu-id="777c0-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="777c0-117">-Profile</span></span>
<span data-ttu-id="777c0-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="777c0-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="777c0-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="777c0-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="777c0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="777c0-120">CommonParameters</span></span>
<span data-ttu-id="777c0-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="777c0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="777c0-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="777c0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="777c0-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="777c0-123">INPUTS</span></span>

## <span data-ttu-id="777c0-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="777c0-124">OUTPUTS</span></span>

## <span data-ttu-id="777c0-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="777c0-125">NOTES</span></span>

## <span data-ttu-id="777c0-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="777c0-126">RELATED LINKS</span></span>

[<span data-ttu-id="777c0-127">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="777c0-127">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


