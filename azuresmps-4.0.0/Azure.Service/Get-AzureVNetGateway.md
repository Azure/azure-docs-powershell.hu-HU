---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4024D20D-46DF-4ED8-A091-E6E17F840E40
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c6ba8827906fbfc51b121e4500dea3ec4555d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016279"
---
# <span data-ttu-id="c9a72-101">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="c9a72-101">Get-AzureVNetGateway</span></span>

## <span data-ttu-id="c9a72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9a72-102">SYNOPSIS</span></span>
<span data-ttu-id="c9a72-103">Virtuális hálózati átjáró állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c9a72-103">Gets the status of a virtual network gateway.</span></span>

## <span data-ttu-id="c9a72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9a72-104">SYNTAX</span></span>

```
Get-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c9a72-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9a72-105">DESCRIPTION</span></span>
<span data-ttu-id="c9a72-106">A **Get-AzureVNetGateway** parancsmag egy meglévő virtuális hálózati átjáró állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c9a72-106">The **Get-AzureVNetGateway** cmdlet gets the status of an existing virtual network gateway.</span></span>

## <span data-ttu-id="c9a72-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c9a72-107">EXAMPLES</span></span>

### <span data-ttu-id="c9a72-108">Példa 1: virtuális hálózati átjáró állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="c9a72-108">Example 1: Get the status of a virtual network gateway</span></span>
```
PS C:\> Get-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="c9a72-109">Ez a parancs azt kapja meg, hogy a virtuális hálózat átjárója a ContosoVN07 nevű virtuális hálózat átjárójának állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9a72-109">This command gets that status of the virtual network gateway for the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="c9a72-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9a72-110">PARAMETERS</span></span>

### <span data-ttu-id="c9a72-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="c9a72-111">-Profile</span></span>
<span data-ttu-id="c9a72-112">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="c9a72-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c9a72-113">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="c9a72-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c9a72-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="c9a72-114">-VNetName</span></span>
<span data-ttu-id="c9a72-115">A virtuális hálózati átjárót tartalmazó virtuális hálózat, amelynek a parancsmagja megkapja az állapotát.</span><span class="sxs-lookup"><span data-stu-id="c9a72-115">Specifies the virtual network that contains the virtual network gateway for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="c9a72-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9a72-116">CommonParameters</span></span>
<span data-ttu-id="c9a72-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9a72-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9a72-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9a72-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9a72-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9a72-119">INPUTS</span></span>

## <span data-ttu-id="c9a72-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9a72-120">OUTPUTS</span></span>

## <span data-ttu-id="c9a72-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9a72-121">NOTES</span></span>

## <span data-ttu-id="c9a72-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9a72-122">RELATED LINKS</span></span>

[<span data-ttu-id="c9a72-123">Új – AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="c9a72-123">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="c9a72-124">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="c9a72-124">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="c9a72-125">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="c9a72-125">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="c9a72-126">Átméretezés-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="c9a72-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="c9a72-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="c9a72-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


