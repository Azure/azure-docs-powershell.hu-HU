---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: 6ff6784bda6bfd9052caa66d04f3f12bc11f568c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667404"
---
# <span data-ttu-id="45d8d-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="45d8d-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="45d8d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="45d8d-103">Hozzáférést biztosít a lemezhez.</span><span class="sxs-lookup"><span data-stu-id="45d8d-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="45d8d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45d8d-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45d8d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="45d8d-105">DESCRIPTION</span></span>
<span data-ttu-id="45d8d-106">A **Grant-AzDiskAccess** parancsmag hozzáférést biztosít a lemezhez.</span><span class="sxs-lookup"><span data-stu-id="45d8d-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="45d8d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="45d8d-107">EXAMPLES</span></span>

### <span data-ttu-id="45d8d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="45d8d-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="45d8d-109">Adjon "READ" hozzáférést a "ResourceGroup01" nevű erőforráscsoport "Disk01" nevű lemezéhez a 60-as másodpercben.</span><span class="sxs-lookup"><span data-stu-id="45d8d-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="45d8d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45d8d-110">PARAMETERS</span></span>

### <span data-ttu-id="45d8d-111">-Access</span><span class="sxs-lookup"><span data-stu-id="45d8d-111">-Access</span></span>
<span data-ttu-id="45d8d-112">Hozzáférési szint megadása</span><span class="sxs-lookup"><span data-stu-id="45d8d-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d8d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45d8d-113">-AsJob</span></span>
<span data-ttu-id="45d8d-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="45d8d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45d8d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45d8d-115">-DefaultProfile</span></span>
<span data-ttu-id="45d8d-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45d8d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45d8d-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="45d8d-117">-DiskName</span></span>
<span data-ttu-id="45d8d-118">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45d8d-118">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45d8d-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="45d8d-119">-DurationInSecond</span></span>
<span data-ttu-id="45d8d-120">A hozzáférési időtartamot másodpercben adja meg.</span><span class="sxs-lookup"><span data-stu-id="45d8d-120">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d8d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45d8d-121">-ResourceGroupName</span></span>
<span data-ttu-id="45d8d-122">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45d8d-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="45d8d-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="45d8d-123">-Confirm</span></span>
<span data-ttu-id="45d8d-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="45d8d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45d8d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45d8d-125">-WhatIf</span></span>
<span data-ttu-id="45d8d-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="45d8d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45d8d-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45d8d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45d8d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d8d-128">CommonParameters</span></span>
<span data-ttu-id="45d8d-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45d8d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d8d-130">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="45d8d-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d8d-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45d8d-131">INPUTS</span></span>

### <span data-ttu-id="45d8d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="45d8d-132">System.String</span></span>

## <span data-ttu-id="45d8d-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45d8d-133">OUTPUTS</span></span>

### <span data-ttu-id="45d8d-134">Microsoft. Azure. commands. számítási. Automation. models. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="45d8d-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="45d8d-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45d8d-135">NOTES</span></span>

## <span data-ttu-id="45d8d-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45d8d-136">RELATED LINKS</span></span>
