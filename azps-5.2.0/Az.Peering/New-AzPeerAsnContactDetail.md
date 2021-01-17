---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: f2bba3b69205585cd6d8f4834803a82bf15ec305
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336089"
---
# <span data-ttu-id="b1401-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="b1401-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="b1401-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1401-102">SYNOPSIS</span></span>
<span data-ttu-id="b1401-103">Létrehozza a PeerAsn-hez a memóriában a névjegy részleteit.</span><span class="sxs-lookup"><span data-stu-id="b1401-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="b1401-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b1401-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1401-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b1401-105">DESCRIPTION</span></span>
<span data-ttu-id="b1401-106">Hozzon létre egy társközi kapcsolati részletet a memóriában.</span><span class="sxs-lookup"><span data-stu-id="b1401-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="b1401-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b1401-107">EXAMPLES</span></span>

### <span data-ttu-id="b1401-108">Kapcsolatfelvételi adatok létrehozása és hozzáadása a PeerAsn-hoz</span><span class="sxs-lookup"><span data-stu-id="b1401-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="b1401-109">Szerepkör és e-mail szükséges.</span><span class="sxs-lookup"><span data-stu-id="b1401-109">Role and email are required.</span></span> <span data-ttu-id="b1401-110">A telefon megadása nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b1401-110">Phone is optional.</span></span> <span data-ttu-id="b1401-111">A telefon támogatja a +-() vagy a szóközöket.</span><span class="sxs-lookup"><span data-stu-id="b1401-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="b1401-112">A PeerAsn-nak tartalmaznia kell legalább egy "Noc" típusú névjegyet.</span><span class="sxs-lookup"><span data-stu-id="b1401-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="b1401-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1401-113">PARAMETERS</span></span>

### <span data-ttu-id="b1401-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1401-114">-DefaultProfile</span></span>
<span data-ttu-id="b1401-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1401-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1401-116">-Email</span><span class="sxs-lookup"><span data-stu-id="b1401-116">-Email</span></span>
<span data-ttu-id="b1401-117">E-mail-címek, amelyek a hálózati üzemeltetési központ problémáinak megoldásához használatosak</span><span class="sxs-lookup"><span data-stu-id="b1401-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="b1401-118">-Telefon</span><span class="sxs-lookup"><span data-stu-id="b1401-118">-Phone</span></span>
<span data-ttu-id="b1401-119">Kapcsolatfelvétel a telefonnal, ha a probléma általában a Network Operations Center (Hálózati műveletközpont) miatt ad problémát</span><span class="sxs-lookup"><span data-stu-id="b1401-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="b1401-120">-Szerepkör</span><span class="sxs-lookup"><span data-stu-id="b1401-120">-Role</span></span>
<span data-ttu-id="b1401-121">Válassza ki a kapcsolattartási adatoknak leginkább megfelelő szerepkört.</span><span class="sxs-lookup"><span data-stu-id="b1401-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="b1401-122">A NOC Contact kötelező.</span><span class="sxs-lookup"><span data-stu-id="b1401-122">NOC Contact is required.</span></span>

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

### <span data-ttu-id="b1401-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1401-123">CommonParameters</span></span>
<span data-ttu-id="b1401-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1401-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1401-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1401-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1401-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1401-126">INPUTS</span></span>

### <span data-ttu-id="b1401-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="b1401-127">None</span></span>

## <span data-ttu-id="b1401-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1401-128">OUTPUTS</span></span>

### <span data-ttu-id="b1401-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="b1401-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="b1401-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b1401-130">NOTES</span></span>

## <span data-ttu-id="b1401-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1401-131">RELATED LINKS</span></span>
