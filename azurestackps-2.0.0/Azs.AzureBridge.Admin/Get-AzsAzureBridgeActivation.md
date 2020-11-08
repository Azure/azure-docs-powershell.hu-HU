---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d47f93addf05af19b523db6ba454443af2c34f
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/26/2020
ms.locfileid: "94017324"
---
# <span data-ttu-id="b75d9-101">Get-AzsAzureBridgeActivation</span><span class="sxs-lookup"><span data-stu-id="b75d9-101">Get-AzsAzureBridgeActivation</span></span>

## <span data-ttu-id="b75d9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b75d9-102">SYNOPSIS</span></span>
<span data-ttu-id="b75d9-103">Az Azure Bridge aktiválását számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b75d9-103">Returns the Azure Bridge Activation.</span></span>

## <span data-ttu-id="b75d9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b75d9-104">SYNTAX</span></span>

### <span data-ttu-id="b75d9-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b75d9-105">List (Default)</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b75d9-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="b75d9-106">Get</span></span>
```
Get-AzsAzureBridgeActivation -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="b75d9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b75d9-107">ResourceId</span></span>
```
Get-AzsAzureBridgeActivation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b75d9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b75d9-108">DESCRIPTION</span></span>
<span data-ttu-id="b75d9-109">Az Azure-köteg regisztrálását követően az aktiválási objektum olyan információkat tartalmaz, amelyek az Azure-alapú bevezetést az Azure rendszerbeli regisztrációhoz csatolják, például a regisztráció lejárati dátuma, a név stb.</span><span class="sxs-lookup"><span data-stu-id="b75d9-109">Once Azure Stack has been registered, the activation object contains information that links an Azure Stack deployment to its registration in Azure, for example, the registration expiration date, name, etc.</span></span>

## <span data-ttu-id="b75d9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b75d9-110">EXAMPLES</span></span>

### <span data-ttu-id="b75d9-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b75d9-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName 'activationRG'
```

<span data-ttu-id="b75d9-112">A "activationRG" erőforráscsoport alatti Azure Bridge-aktiválások listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="b75d9-112">Get a list of Azure Bridge Activations under the resource group "activationRG"</span></span>

### <span data-ttu-id="b75d9-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b75d9-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -Name 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="b75d9-114">Azure-híd aktiválása "myActivation" néven a "activationRG" címszó alatt</span><span class="sxs-lookup"><span data-stu-id="b75d9-114">Get an Azure Bridge Activation by name 'myActivation' situated under 'activationRG'</span></span>

## <span data-ttu-id="b75d9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b75d9-115">PARAMETERS</span></span>

### <span data-ttu-id="b75d9-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b75d9-116">-Name</span></span>
<span data-ttu-id="b75d9-117">Az aktiválás neve.</span><span class="sxs-lookup"><span data-stu-id="b75d9-117">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b75d9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b75d9-118">-ResourceGroupName</span></span>
<span data-ttu-id="b75d9-119">Az Azure-halom regisztrációja során használt erőforráscsoport; Az erőforráscsoportok nevét is megtekintheti a portálon.</span><span class="sxs-lookup"><span data-stu-id="b75d9-119">The Resource Group used during the registration of Azure Stack; you can also view Resource Group names in the portal.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b75d9-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b75d9-120">-ResourceId</span></span>
<span data-ttu-id="b75d9-121">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b75d9-121">The resource id.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b75d9-122">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="b75d9-122">-Skip</span></span>
<span data-ttu-id="b75d9-123">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="b75d9-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b75d9-124">-Top</span><span class="sxs-lookup"><span data-stu-id="b75d9-124">-Top</span></span>
<span data-ttu-id="b75d9-125">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="b75d9-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b75d9-126">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="b75d9-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b75d9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b75d9-127">CommonParameters</span></span>
<span data-ttu-id="b75d9-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b75d9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b75d9-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b75d9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b75d9-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b75d9-130">INPUTS</span></span>

## <span data-ttu-id="b75d9-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b75d9-131">OUTPUTS</span></span>

### <span data-ttu-id="b75d9-132">Microsoft. AzureStack. Management. AzureBridge. admin. models. ActivationResource</span><span class="sxs-lookup"><span data-stu-id="b75d9-132">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ActivationResource</span></span>

## <span data-ttu-id="b75d9-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b75d9-133">NOTES</span></span>

## <span data-ttu-id="b75d9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b75d9-134">RELATED LINKS</span></span>

