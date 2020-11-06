---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
ms.openlocfilehash: fb31bffbdb61c42ea1388c85b71f26af69056c54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495438"
---
# <span data-ttu-id="7b212-101">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7b212-101">Remove-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="7b212-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7b212-102">SYNOPSIS</span></span>
<span data-ttu-id="7b212-103">Eltávolítja az agrár-AEM bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="7b212-103">Removes the AEM extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b212-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7b212-104">SYNTAX</span></span>

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [<CommonParameters>]
```

## <span data-ttu-id="7b212-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7b212-105">DESCRIPTION</span></span>
<span data-ttu-id="7b212-106">A **Remove-AzureRmVMAEMExtension** parancsmag eltávolítja az Azure Enhanced monitoring (AEM) bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="7b212-106">The **Remove-AzureRmVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="7b212-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7b212-107">EXAMPLES</span></span>

### <span data-ttu-id="7b212-108">1. példa: az agrár-AEM bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7b212-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="7b212-109">Ez a parancs eltávolítja a contoso-Server nevű virtuális gép AEM-bővítményét.</span><span class="sxs-lookup"><span data-stu-id="7b212-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="7b212-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7b212-110">PARAMETERS</span></span>

### <span data-ttu-id="7b212-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7b212-111">-Name</span></span>
<span data-ttu-id="7b212-112">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja az AEM-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="7b212-112">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="7b212-113">-OSType</span><span class="sxs-lookup"><span data-stu-id="7b212-113">-OSType</span></span>
<span data-ttu-id="7b212-114">Megadja az operációs rendszer lemezének típusát.</span><span class="sxs-lookup"><span data-stu-id="7b212-114">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="7b212-115">Ha az operációs rendszer lemeze nem tartalmaz típust, akkor ezt a paramétert kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="7b212-115">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="7b212-116">A paraméter elfogadható értékei a következők: Windows és Linux.</span><span class="sxs-lookup"><span data-stu-id="7b212-116">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="7b212-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b212-117">-ResourceGroupName</span></span>
<span data-ttu-id="7b212-118">A virtuális gép erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b212-118">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="7b212-119">Ez a parancsmag eltávolítja az agrár-AEM bővítményt a virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="7b212-119">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="7b212-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="7b212-120">-VMName</span></span>
<span data-ttu-id="7b212-121">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b212-121">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="7b212-122">Ez a parancsmag eltávolítja a virtuális gép AEM bővítményét, amelyre ez a paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b212-122">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="7b212-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b212-123">CommonParameters</span></span>
<span data-ttu-id="7b212-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7b212-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b212-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b212-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b212-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b212-126">INPUTS</span></span>

### <span data-ttu-id="7b212-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="7b212-127">None</span></span>
<span data-ttu-id="7b212-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7b212-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7b212-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b212-129">OUTPUTS</span></span>

## <span data-ttu-id="7b212-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7b212-130">NOTES</span></span>

## <span data-ttu-id="7b212-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b212-131">RELATED LINKS</span></span>

[<span data-ttu-id="7b212-132">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7b212-132">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="7b212-133">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7b212-133">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="7b212-134">Teszt-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7b212-134">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


