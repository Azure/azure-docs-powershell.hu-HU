---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9374f8a55beca561afd9ed4bca4320b685349798
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/22/2020
ms.locfileid: "93851066"
---
# <span data-ttu-id="b069f-101">Get-AzsAzureBridgeActivation</span><span class="sxs-lookup"><span data-stu-id="b069f-101">Get-AzsAzureBridgeActivation</span></span>

## <span data-ttu-id="b069f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b069f-102">SYNOPSIS</span></span>
<span data-ttu-id="b069f-103">Az Azure Bridge aktiválását számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b069f-103">Returns the Azure Bridge Activation.</span></span>

## <span data-ttu-id="b069f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b069f-104">SYNTAX</span></span>

### <span data-ttu-id="b069f-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b069f-105">List (Default)</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b069f-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="b069f-106">Get</span></span>
```
Get-AzsAzureBridgeActivation -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="b069f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b069f-107">ResourceId</span></span>
```
Get-AzsAzureBridgeActivation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b069f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b069f-108">DESCRIPTION</span></span>
<span data-ttu-id="b069f-109">Az Azure-köteg regisztrálását követően az aktiválási objektum olyan információkat tartalmaz, amelyek az Azure-alapú bevezetést az Azure rendszerbeli regisztrációhoz csatolják, például a regisztráció lejárati dátuma, a név stb.</span><span class="sxs-lookup"><span data-stu-id="b069f-109">Once Azure Stack has been registered, the activation object contains information that links an Azure Stack deployment to its registration in Azure, for example, the registration expiration date, name, etc.</span></span>

## <span data-ttu-id="b069f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b069f-110">EXAMPLES</span></span>

### <span data-ttu-id="b069f-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="b069f-111">EXAMPLE 1</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName 'activationRG'
```

<span data-ttu-id="b069f-112">A "activationRG" erőforráscsoport alatti Azure Bridge-aktiválások listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="b069f-112">Get a list of Azure Bridge Activations under the resource group "activationRG"</span></span>

### <span data-ttu-id="b069f-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="b069f-113">EXAMPLE 2</span></span>
```
Get-AzsAzureBridgeActivation -Name 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="b069f-114">Azure-híd aktiválása "myActivation" néven a "activationRG" címszó alatt</span><span class="sxs-lookup"><span data-stu-id="b069f-114">Get an Azure Bridge Activation by name 'myActivation' situated under 'activationRG'</span></span>

## <span data-ttu-id="b069f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b069f-115">PARAMETERS</span></span>

### <span data-ttu-id="b069f-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b069f-116">-Name</span></span>
<span data-ttu-id="b069f-117">Az aktiválás neve.</span><span class="sxs-lookup"><span data-stu-id="b069f-117">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b069f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b069f-118">-ResourceGroupName</span></span>
<span data-ttu-id="b069f-119">Az Azure-halom regisztrációja során használt erőforráscsoport; Az erőforráscsoportok nevét is megtekintheti a portálon.</span><span class="sxs-lookup"><span data-stu-id="b069f-119">The Resource Group used during the registration of Azure Stack; you can also view Resource Group names in the portal.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b069f-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b069f-120">-ResourceId</span></span>
<span data-ttu-id="b069f-121">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b069f-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b069f-122">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="b069f-122">-Skip</span></span>
<span data-ttu-id="b069f-123">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="b069f-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b069f-124">-Top</span><span class="sxs-lookup"><span data-stu-id="b069f-124">-Top</span></span>
<span data-ttu-id="b069f-125">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="b069f-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b069f-126">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="b069f-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b069f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b069f-127">CommonParameters</span></span>
<span data-ttu-id="b069f-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b069f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b069f-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b069f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b069f-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b069f-130">INPUTS</span></span>

## <span data-ttu-id="b069f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b069f-131">OUTPUTS</span></span>

### <span data-ttu-id="b069f-132">Microsoft. AzureStack. Management. AzureBridge. admin. models. ActivationResource</span><span class="sxs-lookup"><span data-stu-id="b069f-132">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ActivationResource</span></span>

## <span data-ttu-id="b069f-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b069f-133">NOTES</span></span>

## <span data-ttu-id="b069f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b069f-134">RELATED LINKS</span></span>
