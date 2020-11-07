---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaemextension
schema: 2.0.0
ms.openlocfilehash: cf70191c47f3778268b0087ea542a6812155ebbb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850065"
---
# <span data-ttu-id="ec220-101">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ec220-101">Remove-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="ec220-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec220-102">SYNOPSIS</span></span>
<span data-ttu-id="ec220-103">Eltávolítja az agrár-AEM bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="ec220-103">Removes the AEM extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec220-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec220-104">SYNTAX</span></span>

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec220-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec220-105">DESCRIPTION</span></span>
<span data-ttu-id="ec220-106">A **Remove-AzureRmVMAEMExtension** parancsmag eltávolítja az Azure Enhanced monitoring (AEM) bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="ec220-106">The **Remove-AzureRmVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="ec220-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ec220-107">EXAMPLES</span></span>

### <span data-ttu-id="ec220-108">1. példa: az agrár-AEM bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ec220-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="ec220-109">Ez a parancs eltávolítja a contoso-Server nevű virtuális gép AEM-bővítményét.</span><span class="sxs-lookup"><span data-stu-id="ec220-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="ec220-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec220-110">PARAMETERS</span></span>

### <span data-ttu-id="ec220-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec220-111">-DefaultProfile</span></span>
<span data-ttu-id="ec220-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec220-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec220-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ec220-113">-Name</span></span>
<span data-ttu-id="ec220-114">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja az AEM-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="ec220-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec220-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="ec220-115">-OSType</span></span>
<span data-ttu-id="ec220-116">Megadja az operációs rendszer lemezének típusát.</span><span class="sxs-lookup"><span data-stu-id="ec220-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="ec220-117">Ha az operációs rendszer lemeze nem tartalmaz típust, akkor ezt a paramétert kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="ec220-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="ec220-118">A paraméter elfogadható értékei a következők: Windows és Linux.</span><span class="sxs-lookup"><span data-stu-id="ec220-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec220-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec220-119">-ResourceGroupName</span></span>
<span data-ttu-id="ec220-120">A virtuális gép erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec220-120">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="ec220-121">Ez a parancsmag eltávolítja az agrár-AEM bővítményt a virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="ec220-121">This cmdlet removes the AEM extension from that virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec220-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="ec220-122">-VMName</span></span>
<span data-ttu-id="ec220-123">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec220-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ec220-124">Ez a parancsmag eltávolítja a virtuális gép AEM bővítményét, amelyre ez a paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec220-124">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec220-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec220-125">CommonParameters</span></span>
<span data-ttu-id="ec220-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec220-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec220-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec220-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec220-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec220-128">INPUTS</span></span>

### <span data-ttu-id="ec220-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="ec220-129">None</span></span>
<span data-ttu-id="ec220-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ec220-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ec220-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec220-131">OUTPUTS</span></span>

### <span data-ttu-id="ec220-132">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ec220-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ec220-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec220-133">NOTES</span></span>

## <span data-ttu-id="ec220-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec220-134">RELATED LINKS</span></span>

[<span data-ttu-id="ec220-135">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ec220-135">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="ec220-136">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ec220-136">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="ec220-137">Teszt-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ec220-137">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


