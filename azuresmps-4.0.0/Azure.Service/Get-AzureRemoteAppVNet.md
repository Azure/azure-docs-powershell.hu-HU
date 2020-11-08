---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 58DABEB0-D3B6-478B-9B83-80E4C67A7792
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d4717e795bcfea9728cbabb1b7c788713907aaa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016570"
---
# <span data-ttu-id="386e1-101">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="386e1-101">Get-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="386e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="386e1-102">SYNOPSIS</span></span>
<span data-ttu-id="386e1-103">Információt keres az Azure RemoteApp virtuális hálózatáról az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="386e1-103">Retrieves information about Azure RemoteApp virtual networks in Azure.</span></span>

## <span data-ttu-id="386e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="386e1-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVNet [[-VNetName] <String>] [-IncludeSharedKey] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="386e1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="386e1-105">DESCRIPTION</span></span>
<span data-ttu-id="386e1-106">A **Get-AzureRemoteAppVNet** parancsmag információkat keres az Azure RemoteApp virtuális hálózatokról a Microsoft Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="386e1-106">The **Get-AzureRemoteAppVNet** cmdlet retrieves information about Azure RemoteApp virtual networks in Microsoft Azure.</span></span>
<span data-ttu-id="386e1-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely a megadott virtuális hálózatról tartalmaz információkat.</span><span class="sxs-lookup"><span data-stu-id="386e1-107">This cmdlet returns an object that contains information about a specified virtual network.</span></span>
<span data-ttu-id="386e1-108">Ha nincs megadva virtuális hálózat, ez a parancsmag információt ad az aktuális előfizetésben lévő összes virtuális hálózatról.</span><span class="sxs-lookup"><span data-stu-id="386e1-108">If no virtual network is specified, this cmdlet returns information about all the virtual networks in the current subscription.</span></span>

## <span data-ttu-id="386e1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="386e1-109">EXAMPLES</span></span>

### <span data-ttu-id="386e1-110">Példa 1: virtuális hálózat adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="386e1-110">Example 1: Retrieve information about a virtual network</span></span>
```
PS C:\> Get-AzureRemoteAppVNet -VNetName "ContosoVNet"
```

<span data-ttu-id="386e1-111">Ez a parancs információkat kap a ContosoVNet nevű virtuális hálózatról.</span><span class="sxs-lookup"><span data-stu-id="386e1-111">This command gets information about the virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="386e1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="386e1-112">PARAMETERS</span></span>

### <span data-ttu-id="386e1-113">-IncludeSharedKey</span><span class="sxs-lookup"><span data-stu-id="386e1-113">-IncludeSharedKey</span></span>
<span data-ttu-id="386e1-114">Azt jelzi, hogy ez a parancsmag a virtuális hálózatról beolvasott adatok megosztott kulcs értékét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="386e1-114">Indicates that this cmdlet includes the shared key value in the information it retrieves about the virtual network.</span></span>

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

### <span data-ttu-id="386e1-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="386e1-115">-Profile</span></span>
<span data-ttu-id="386e1-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="386e1-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="386e1-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="386e1-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="386e1-118">-VNetName</span><span class="sxs-lookup"><span data-stu-id="386e1-118">-VNetName</span></span>
<span data-ttu-id="386e1-119">Az Azure RemoteApp virtuális hálózatának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="386e1-119">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="386e1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="386e1-120">CommonParameters</span></span>
<span data-ttu-id="386e1-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="386e1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="386e1-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="386e1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="386e1-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="386e1-123">INPUTS</span></span>

## <span data-ttu-id="386e1-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="386e1-124">OUTPUTS</span></span>

## <span data-ttu-id="386e1-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="386e1-125">NOTES</span></span>

## <span data-ttu-id="386e1-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="386e1-126">RELATED LINKS</span></span>

[<span data-ttu-id="386e1-127">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="386e1-127">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


