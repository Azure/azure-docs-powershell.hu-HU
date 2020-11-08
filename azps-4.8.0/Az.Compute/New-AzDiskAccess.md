---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
ms.openlocfilehash: 430c0d09c56aa4fb57399c97714dc70cb19dd500
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183118"
---
# <span data-ttu-id="61ca8-101">New-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="61ca8-101">New-AzDiskAccess</span></span>

## <span data-ttu-id="61ca8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="61ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="61ca8-103">Disk Access-erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="61ca8-103">Creates a Disk Access resource</span></span>

## <span data-ttu-id="61ca8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="61ca8-104">SYNTAX</span></span>

```
New-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61ca8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="61ca8-105">DESCRIPTION</span></span>
<span data-ttu-id="61ca8-106">A **New-AzDiskAccess** parancsmag létrehoz egy Disk Access-erőforrást</span><span class="sxs-lookup"><span data-stu-id="61ca8-106">The **New-AzDiskAccess** cmdlet creates a Disk Access resource</span></span>

## <span data-ttu-id="61ca8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="61ca8-107">EXAMPLES</span></span>

### <span data-ttu-id="61ca8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="61ca8-108">Example 1</span></span>
```
PS C:\> New-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" -Location "NorthCentralUS"
```

<span data-ttu-id="61ca8-109">Ez a parancs a megadott tulajdonságokkal rendelkező lemez-hozzáférést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="61ca8-109">This command will create a Disk Access with given properties.</span></span> 

## <span data-ttu-id="61ca8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="61ca8-110">PARAMETERS</span></span>

### <span data-ttu-id="61ca8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61ca8-111">-AsJob</span></span>
<span data-ttu-id="61ca8-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="61ca8-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ca8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61ca8-113">-DefaultProfile</span></span>
<span data-ttu-id="61ca8-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="61ca8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61ca8-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="61ca8-115">-Location</span></span>
<span data-ttu-id="61ca8-116">A helyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="61ca8-116">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61ca8-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="61ca8-117">-Name</span></span>
<span data-ttu-id="61ca8-118">A lemez elérési útjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="61ca8-118">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61ca8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61ca8-119">-ResourceGroupName</span></span>
<span data-ttu-id="61ca8-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="61ca8-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61ca8-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="61ca8-121">-Confirm</span></span>
<span data-ttu-id="61ca8-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="61ca8-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ca8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61ca8-123">-WhatIf</span></span>
<span data-ttu-id="61ca8-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="61ca8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61ca8-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="61ca8-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ca8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ca8-126">CommonParameters</span></span>
<span data-ttu-id="61ca8-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="61ca8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ca8-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="61ca8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ca8-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="61ca8-129">INPUTS</span></span>

### <span data-ttu-id="61ca8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="61ca8-130">System.String</span></span>

## <span data-ttu-id="61ca8-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61ca8-131">OUTPUTS</span></span>

### <span data-ttu-id="61ca8-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="61ca8-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="61ca8-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="61ca8-133">NOTES</span></span>

## <span data-ttu-id="61ca8-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61ca8-134">RELATED LINKS</span></span>
