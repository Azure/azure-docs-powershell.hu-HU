---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4E19A767-8233-42A0-95C5-1547B4DF297E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c08105f8083b6b2e132c3b8e61c92627572305
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016334"
---
# <span data-ttu-id="5551f-101">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5551f-101">Get-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="5551f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5551f-102">SYNOPSIS</span></span>
<span data-ttu-id="5551f-103">Megkeresi a hálózat biztonsági csoportjának részleteit.</span><span class="sxs-lookup"><span data-stu-id="5551f-103">Gets details for a network security group.</span></span>

## <span data-ttu-id="5551f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5551f-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroup [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5551f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5551f-105">DESCRIPTION</span></span>
<span data-ttu-id="5551f-106">A **Get-AzureNetworkSecurityGroup** parancsmag információt ad az Azure hálózat biztonsági csoportjairól.</span><span class="sxs-lookup"><span data-stu-id="5551f-106">The **Get-AzureNetworkSecurityGroup** cmdlet returns details for an Azure network security group.</span></span>
<span data-ttu-id="5551f-107">A hálózati biztonsági szabályok megjelenítéséhez adja meg a *részletes* paramétert.</span><span class="sxs-lookup"><span data-stu-id="5551f-107">Specify the *Detailed* parameter to display the network security rules.</span></span>

## <span data-ttu-id="5551f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5551f-108">EXAMPLES</span></span>

## <span data-ttu-id="5551f-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5551f-109">PARAMETERS</span></span>

### <span data-ttu-id="5551f-110">– Részletes</span><span class="sxs-lookup"><span data-stu-id="5551f-110">-Detailed</span></span>
<span data-ttu-id="5551f-111">Jelzi, hogy ez a parancsmag a hálózatbiztonsági csoport hálózati biztonsági szabályait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="5551f-111">Indicates that this cmdlet returns the network security rules for the network security group.</span></span>

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

### <span data-ttu-id="5551f-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5551f-112">-Name</span></span>
<span data-ttu-id="5551f-113">Annak a hálózati biztonsági csoportnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="5551f-113">Specifies the name of the network security group that this cmdlet gets.</span></span>

> [!NOTE]
> <span data-ttu-id="5551f-114">Ha egy klasszikus hálózati biztonsági csoportot az Azure portálon kívüli ***alapértelmezett hálózati*** kapcsolaton kívüli csoportba hoz létre, a következő PowerShell-szintaxist kell `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'` használnia:</span><span class="sxs-lookup"><span data-stu-id="5551f-114">When a classic network security group is created in a resource group other than ***Default-Networking*** using the Azure portal, you must use the following PowerShell syntax: `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'`.</span></span>

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

### <span data-ttu-id="5551f-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="5551f-115">-Profile</span></span>
<span data-ttu-id="5551f-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="5551f-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5551f-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="5551f-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5551f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5551f-118">CommonParameters</span></span>
<span data-ttu-id="5551f-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5551f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5551f-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5551f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5551f-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5551f-121">INPUTS</span></span>

## <span data-ttu-id="5551f-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5551f-122">OUTPUTS</span></span>

## <span data-ttu-id="5551f-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5551f-123">NOTES</span></span>

## <span data-ttu-id="5551f-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5551f-124">RELATED LINKS</span></span>

[<span data-ttu-id="5551f-125">Új – AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5551f-125">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="5551f-126">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5551f-126">Remove-AzureNetworkSecurityGroup</span></span>](./Remove-AzureNetworkSecurityGroup.md)

