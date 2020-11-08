---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D61E0D1A-7A79-436C-BB1B-740E31BC982D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49aa46cf44d07e9063f819d6ba90788e0fb221fa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015910"
---
# <span data-ttu-id="78233-101">New-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78233-101">New-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="78233-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78233-102">SYNOPSIS</span></span>
<span data-ttu-id="78233-103">Azure-hálózati biztonsági csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="78233-103">Creates an Azure network security group.</span></span>

## <span data-ttu-id="78233-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78233-104">SYNTAX</span></span>

```
New-AzureNetworkSecurityGroup -Name <String> -Location <String> [-Label <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="78233-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="78233-105">DESCRIPTION</span></span>
<span data-ttu-id="78233-106">A **New-AzureNetworkSecurityGroup** parancsmag az Azure hálózat biztonsági csoportját hozza létre egy helyen.</span><span class="sxs-lookup"><span data-stu-id="78233-106">The **New-AzureNetworkSecurityGroup** cmdlet creates an Azure network security group in a location.</span></span>

## <span data-ttu-id="78233-107">Példák</span><span class="sxs-lookup"><span data-stu-id="78233-107">EXAMPLES</span></span>

## <span data-ttu-id="78233-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78233-108">PARAMETERS</span></span>

### <span data-ttu-id="78233-109">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="78233-109">-Label</span></span>
<span data-ttu-id="78233-110">Az új hálózati biztonsági csoport leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="78233-110">Specifies a description for the new network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78233-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="78233-111">-Location</span></span>
<span data-ttu-id="78233-112">Azt az Azure-helyet adja meg, ahol a parancsmag hálózati biztonsági csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="78233-112">Specifies the Azure location in which this cmdlet creates a network security group.</span></span>
<span data-ttu-id="78233-113">Ha érvényes helyeket szeretne beolvasni, használja az Get-AzureLocation parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="78233-113">To obtain valid locations, use the Get-AzureLocation cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78233-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="78233-114">-Name</span></span>
<span data-ttu-id="78233-115">Az új hálózati biztonsági csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="78233-115">Specifies a name for the new network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78233-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="78233-116">-Profile</span></span>
<span data-ttu-id="78233-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="78233-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="78233-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="78233-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="78233-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78233-119">CommonParameters</span></span>
<span data-ttu-id="78233-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78233-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78233-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78233-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78233-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78233-122">INPUTS</span></span>

## <span data-ttu-id="78233-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78233-123">OUTPUTS</span></span>

## <span data-ttu-id="78233-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78233-124">NOTES</span></span>

## <span data-ttu-id="78233-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78233-125">RELATED LINKS</span></span>

[<span data-ttu-id="78233-126">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78233-126">Get-AzureNetworkSecurityGroup</span></span>](./Get-AzureNetworkSecurityGroup.md)


