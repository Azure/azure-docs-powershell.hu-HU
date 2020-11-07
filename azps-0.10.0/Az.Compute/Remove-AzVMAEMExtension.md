---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 224d11aba6eece63c7c080415253b4833c665cee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844417"
---
# <span data-ttu-id="abf73-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="abf73-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="abf73-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="abf73-102">SYNOPSIS</span></span>
<span data-ttu-id="abf73-103">Eltávolítja az agrár-AEM bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="abf73-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="abf73-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="abf73-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abf73-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="abf73-105">DESCRIPTION</span></span>
<span data-ttu-id="abf73-106">A **Remove-AzVMAEMExtension** parancsmag eltávolítja az Azure Enhanced monitoring (AEM) bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="abf73-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="abf73-107">Példák</span><span class="sxs-lookup"><span data-stu-id="abf73-107">EXAMPLES</span></span>

### <span data-ttu-id="abf73-108">1. példa: az agrár-AEM bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="abf73-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="abf73-109">Ez a parancs eltávolítja a contoso-Server nevű virtuális gép AEM-bővítményét.</span><span class="sxs-lookup"><span data-stu-id="abf73-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="abf73-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="abf73-110">PARAMETERS</span></span>

### <span data-ttu-id="abf73-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf73-111">-DefaultProfile</span></span>
<span data-ttu-id="abf73-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="abf73-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abf73-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="abf73-113">-Name</span></span>
<span data-ttu-id="abf73-114">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja az AEM-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="abf73-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="abf73-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="abf73-115">-OSType</span></span>
<span data-ttu-id="abf73-116">Megadja az operációs rendszer lemezének típusát.</span><span class="sxs-lookup"><span data-stu-id="abf73-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="abf73-117">Ha az operációs rendszer lemeze nem tartalmaz típust, akkor ezt a paramétert kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="abf73-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="abf73-118">A paraméter elfogadható értékei a következők: Windows és Linux.</span><span class="sxs-lookup"><span data-stu-id="abf73-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="abf73-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf73-119">-ResourceGroupName</span></span>
<span data-ttu-id="abf73-120">A virtuális gép erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="abf73-120">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="abf73-121">Ez a parancsmag eltávolítja az agrár-AEM bővítményt a virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="abf73-121">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="abf73-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="abf73-122">-VMName</span></span>
<span data-ttu-id="abf73-123">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="abf73-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="abf73-124">Ez a parancsmag eltávolítja a virtuális gép AEM bővítményét, amelyre ez a paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="abf73-124">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="abf73-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf73-125">CommonParameters</span></span>
<span data-ttu-id="abf73-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="abf73-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf73-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abf73-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf73-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="abf73-128">INPUTS</span></span>

### <span data-ttu-id="abf73-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="abf73-129">None</span></span>
<span data-ttu-id="abf73-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="abf73-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="abf73-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abf73-131">OUTPUTS</span></span>

### <span data-ttu-id="abf73-132">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="abf73-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="abf73-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="abf73-133">NOTES</span></span>

## <span data-ttu-id="abf73-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abf73-134">RELATED LINKS</span></span>

[<span data-ttu-id="abf73-135">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="abf73-135">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="abf73-136">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="abf73-136">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="abf73-137">Teszt-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="abf73-137">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


