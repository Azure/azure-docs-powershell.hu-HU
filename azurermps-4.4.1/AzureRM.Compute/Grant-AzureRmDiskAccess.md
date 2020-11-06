---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
ms.openlocfilehash: a1b06a870822f2fef0bf2f9a39321c13642f8cad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505639"
---
# <span data-ttu-id="74001-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="74001-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="74001-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="74001-102">SYNOPSIS</span></span>
<span data-ttu-id="74001-103">Hozzáférést biztosít a lemezhez.</span><span class="sxs-lookup"><span data-stu-id="74001-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74001-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="74001-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74001-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="74001-105">DESCRIPTION</span></span>
<span data-ttu-id="74001-106">A **Grant-AzureRmDiskAccess** parancsmag hozzáférést biztosít a lemezhez.</span><span class="sxs-lookup"><span data-stu-id="74001-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="74001-107">Példák</span><span class="sxs-lookup"><span data-stu-id="74001-107">EXAMPLES</span></span>

### <span data-ttu-id="74001-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="74001-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="74001-109">Adjon "READ" hozzáférést a "ResourceGroup01" nevű erőforráscsoport "Disk01" nevű lemezéhez a 60-as másodpercben.</span><span class="sxs-lookup"><span data-stu-id="74001-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="74001-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="74001-110">PARAMETERS</span></span>

### <span data-ttu-id="74001-111">-Access</span><span class="sxs-lookup"><span data-stu-id="74001-111">-Access</span></span>
<span data-ttu-id="74001-112">Hozzáférési szint megadása</span><span class="sxs-lookup"><span data-stu-id="74001-112">Specifies Access level.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74001-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74001-113">-DefaultProfile</span></span>
<span data-ttu-id="74001-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74001-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74001-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="74001-115">-DiskName</span></span>
<span data-ttu-id="74001-116">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="74001-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="74001-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="74001-117">-DurationInSecond</span></span>
<span data-ttu-id="74001-118">A hozzáférési időtartamot másodpercben adja meg.</span><span class="sxs-lookup"><span data-stu-id="74001-118">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="74001-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74001-119">-ResourceGroupName</span></span>
<span data-ttu-id="74001-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="74001-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="74001-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="74001-121">-Confirm</span></span>
<span data-ttu-id="74001-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="74001-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74001-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74001-123">-WhatIf</span></span>
<span data-ttu-id="74001-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="74001-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74001-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="74001-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74001-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74001-126">CommonParameters</span></span>
<span data-ttu-id="74001-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="74001-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74001-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74001-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74001-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="74001-129">INPUTS</span></span>

### <span data-ttu-id="74001-130">System. String</span><span class="sxs-lookup"><span data-stu-id="74001-130">System.String</span></span>

## <span data-ttu-id="74001-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74001-131">OUTPUTS</span></span>

### <span data-ttu-id="74001-132">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="74001-132">System.Object</span></span>

## <span data-ttu-id="74001-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="74001-133">NOTES</span></span>

## <span data-ttu-id="74001-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74001-134">RELATED LINKS</span></span>

