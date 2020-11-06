---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Grant-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Grant-AzureRmDiskAccess.md
ms.openlocfilehash: ae45dadd2d5af2cf81a8735ca6725ee4798dbf29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499700"
---
# <span data-ttu-id="87916-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="87916-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="87916-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87916-102">SYNOPSIS</span></span>
<span data-ttu-id="87916-103">Hozzáférést biztosít a lemezhez.</span><span class="sxs-lookup"><span data-stu-id="87916-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87916-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87916-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87916-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="87916-105">DESCRIPTION</span></span>
<span data-ttu-id="87916-106">A **Grant-AzureRmDiskAccess** parancsmag hozzáférést biztosít a lemezhez.</span><span class="sxs-lookup"><span data-stu-id="87916-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="87916-107">Példák</span><span class="sxs-lookup"><span data-stu-id="87916-107">EXAMPLES</span></span>

### <span data-ttu-id="87916-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="87916-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="87916-109">Adjon "READ" hozzáférést a "ResourceGroup01" nevű erőforráscsoport "Disk01" nevű lemezéhez a 60-as másodpercben.</span><span class="sxs-lookup"><span data-stu-id="87916-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="87916-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87916-110">PARAMETERS</span></span>

### <span data-ttu-id="87916-111">-Access</span><span class="sxs-lookup"><span data-stu-id="87916-111">-Access</span></span>
<span data-ttu-id="87916-112">Hozzáférési szint megadása</span><span class="sxs-lookup"><span data-stu-id="87916-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87916-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87916-113">-AsJob</span></span>
<span data-ttu-id="87916-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="87916-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="87916-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87916-115">-DefaultProfile</span></span>
<span data-ttu-id="87916-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87916-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87916-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="87916-117">-DiskName</span></span>
<span data-ttu-id="87916-118">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87916-118">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87916-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="87916-119">-DurationInSecond</span></span>
<span data-ttu-id="87916-120">A hozzáférési időtartamot másodpercben adja meg.</span><span class="sxs-lookup"><span data-stu-id="87916-120">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87916-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87916-121">-ResourceGroupName</span></span>
<span data-ttu-id="87916-122">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87916-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87916-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="87916-123">-Confirm</span></span>
<span data-ttu-id="87916-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="87916-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87916-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87916-125">-WhatIf</span></span>
<span data-ttu-id="87916-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="87916-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87916-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="87916-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87916-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87916-128">CommonParameters</span></span>
<span data-ttu-id="87916-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87916-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87916-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87916-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87916-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87916-131">INPUTS</span></span>

### <span data-ttu-id="87916-132">System. String</span><span class="sxs-lookup"><span data-stu-id="87916-132">System.String</span></span>

## <span data-ttu-id="87916-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87916-133">OUTPUTS</span></span>

### <span data-ttu-id="87916-134">Microsoft. Azure. commands. számítási. Automation. models. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="87916-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="87916-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87916-135">NOTES</span></span>

## <span data-ttu-id="87916-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87916-136">RELATED LINKS</span></span>
