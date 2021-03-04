---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: 978c513646c08577f4fa15b8a0e460320878c7c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937705"
---
# <span data-ttu-id="4fc81-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="4fc81-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="4fc81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fc81-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc81-103">Létrehozza a PeerAsn-hez a memóriában a névjegy részleteit.</span><span class="sxs-lookup"><span data-stu-id="4fc81-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="4fc81-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4fc81-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fc81-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4fc81-105">DESCRIPTION</span></span>
<span data-ttu-id="4fc81-106">Hozzon létre egy társközi kapcsolati részletet a memóriában.</span><span class="sxs-lookup"><span data-stu-id="4fc81-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="4fc81-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4fc81-107">EXAMPLES</span></span>

### <span data-ttu-id="4fc81-108">Kapcsolatfelvételi adatok létrehozása és hozzáadása a PeerAsn-hoz</span><span class="sxs-lookup"><span data-stu-id="4fc81-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="4fc81-109">Szerepkör és e-mail szükséges.</span><span class="sxs-lookup"><span data-stu-id="4fc81-109">Role and email are required.</span></span> <span data-ttu-id="4fc81-110">A telefon megadása nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4fc81-110">Phone is optional.</span></span> <span data-ttu-id="4fc81-111">A telefon támogatja a +-() vagy a szóközöket.</span><span class="sxs-lookup"><span data-stu-id="4fc81-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="4fc81-112">A PeerAsn-nak tartalmaznia kell legalább egy "Noc" típusú névjegyet.</span><span class="sxs-lookup"><span data-stu-id="4fc81-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="4fc81-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fc81-113">PARAMETERS</span></span>

### <span data-ttu-id="4fc81-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fc81-114">-DefaultProfile</span></span>
<span data-ttu-id="4fc81-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4fc81-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fc81-116">-Email</span><span class="sxs-lookup"><span data-stu-id="4fc81-116">-Email</span></span>
<span data-ttu-id="4fc81-117">E-mail-címek, amelyek a hálózati üzemeltetési központ problémáinak megoldásához használatosak</span><span class="sxs-lookup"><span data-stu-id="4fc81-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="4fc81-118">-Telefon</span><span class="sxs-lookup"><span data-stu-id="4fc81-118">-Phone</span></span>
<span data-ttu-id="4fc81-119">Kapcsolatfelvétel a telefonnal, ha a probléma általában a Network Operations Center (Hálózati műveletközpont) miatt ad problémát</span><span class="sxs-lookup"><span data-stu-id="4fc81-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="4fc81-120">-Szerepkör</span><span class="sxs-lookup"><span data-stu-id="4fc81-120">-Role</span></span>
<span data-ttu-id="4fc81-121">Válassza ki a kapcsolattartási adatoknak leginkább megfelelő szerepkört.</span><span class="sxs-lookup"><span data-stu-id="4fc81-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="4fc81-122">A NOC Contact kötelező.</span><span class="sxs-lookup"><span data-stu-id="4fc81-122">NOC Contact is required.</span></span>

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

### <span data-ttu-id="4fc81-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc81-123">CommonParameters</span></span>
<span data-ttu-id="4fc81-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fc81-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc81-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4fc81-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc81-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4fc81-126">INPUTS</span></span>

### <span data-ttu-id="4fc81-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="4fc81-127">None</span></span>

## <span data-ttu-id="4fc81-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fc81-128">OUTPUTS</span></span>

### <span data-ttu-id="4fc81-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="4fc81-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="4fc81-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4fc81-130">NOTES</span></span>

## <span data-ttu-id="4fc81-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fc81-131">RELATED LINKS</span></span>
