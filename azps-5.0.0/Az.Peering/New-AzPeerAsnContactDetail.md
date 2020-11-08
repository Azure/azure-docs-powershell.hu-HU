---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: f2bba3b69205585cd6d8f4834803a82bf15ec305
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186369"
---
# <span data-ttu-id="a9976-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="a9976-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="a9976-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9976-102">SYNOPSIS</span></span>
<span data-ttu-id="a9976-103">A PeerAsn-ban a memória-kapcsolat részleteit hozza létre.</span><span class="sxs-lookup"><span data-stu-id="a9976-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="a9976-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9976-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9976-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9976-105">DESCRIPTION</span></span>
<span data-ttu-id="a9976-106">Hozzon létre egy a Memory PeerAsn-adatait.</span><span class="sxs-lookup"><span data-stu-id="a9976-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="a9976-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a9976-107">EXAMPLES</span></span>

### <span data-ttu-id="a9976-108">A partnerek részleteinek létrehozása és hozzáadása a PeerAsn-hoz</span><span class="sxs-lookup"><span data-stu-id="a9976-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="a9976-109">Szerepkör és e-mail-cím szükséges.</span><span class="sxs-lookup"><span data-stu-id="a9976-109">Role and email are required.</span></span> <span data-ttu-id="a9976-110">A telefon nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="a9976-110">Phone is optional.</span></span> <span data-ttu-id="a9976-111">A telefon támogatja a +-() vagy a szóközöket.</span><span class="sxs-lookup"><span data-stu-id="a9976-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="a9976-112">A PeerAsn tartalmaznia kell legalább egy, a "Noc" típusú adatot.</span><span class="sxs-lookup"><span data-stu-id="a9976-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="a9976-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9976-113">PARAMETERS</span></span>

### <span data-ttu-id="a9976-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9976-114">-DefaultProfile</span></span>
<span data-ttu-id="a9976-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9976-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9976-116">– E-mail</span><span class="sxs-lookup"><span data-stu-id="a9976-116">-Email</span></span>
<span data-ttu-id="a9976-117">A kapcsolathoz használt e-mail-címek, ha a problémák származhat belőle jellemzően hálózati műveleti központ</span><span class="sxs-lookup"><span data-stu-id="a9976-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9976-118">-Telefon</span><span class="sxs-lookup"><span data-stu-id="a9976-118">-Phone</span></span>
<span data-ttu-id="a9976-119">Telefonos kapcsolat, ha a problémák származhat belőle jellemzően hálózati műveleti központot használ</span><span class="sxs-lookup"><span data-stu-id="a9976-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9976-120">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="a9976-120">-Role</span></span>
<span data-ttu-id="a9976-121">Válassza ki azt a szerepkört, amely a legjobban megfelel a névjegykártyán szereplő adatoknak.</span><span class="sxs-lookup"><span data-stu-id="a9976-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="a9976-122">NOC-kontaktusra van szükség.</span><span class="sxs-lookup"><span data-stu-id="a9976-122">NOC Contact is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9976-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9976-123">CommonParameters</span></span>
<span data-ttu-id="a9976-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9976-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9976-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a9976-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9976-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9976-126">INPUTS</span></span>

### <span data-ttu-id="a9976-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="a9976-127">None</span></span>

## <span data-ttu-id="a9976-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9976-128">OUTPUTS</span></span>

### <span data-ttu-id="a9976-129">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="a9976-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="a9976-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9976-130">NOTES</span></span>

## <span data-ttu-id="a9976-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9976-131">RELATED LINKS</span></span>
