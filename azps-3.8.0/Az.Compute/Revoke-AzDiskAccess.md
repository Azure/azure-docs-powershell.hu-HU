---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 76fb2e7483bb510d5eceb92b51f7e5e538c3b22b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012099"
---
# <span data-ttu-id="03bd1-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="03bd1-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="03bd1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03bd1-102">SYNOPSIS</span></span>
<span data-ttu-id="03bd1-103">Hozzáférés visszavonása a lemezhez</span><span class="sxs-lookup"><span data-stu-id="03bd1-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="03bd1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03bd1-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03bd1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="03bd1-105">DESCRIPTION</span></span>
<span data-ttu-id="03bd1-106">A **Visszavonás-AzDiskAccess** parancsmag visszavonja a lemezhez való hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="03bd1-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="03bd1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="03bd1-107">EXAMPLES</span></span>

### <span data-ttu-id="03bd1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="03bd1-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="03bd1-109">A "ResourceGroup01" nevű erőforráscsoport "Disk01" nevű lemezéhez való hozzáférés visszavonása</span><span class="sxs-lookup"><span data-stu-id="03bd1-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="03bd1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03bd1-110">PARAMETERS</span></span>

### <span data-ttu-id="03bd1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03bd1-111">-AsJob</span></span>
<span data-ttu-id="03bd1-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="03bd1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03bd1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03bd1-113">-DefaultProfile</span></span>
<span data-ttu-id="03bd1-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03bd1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03bd1-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="03bd1-115">-DiskName</span></span>
<span data-ttu-id="03bd1-116">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="03bd1-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="03bd1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03bd1-117">-ResourceGroupName</span></span>
<span data-ttu-id="03bd1-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="03bd1-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="03bd1-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="03bd1-119">-Confirm</span></span>
<span data-ttu-id="03bd1-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="03bd1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03bd1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03bd1-121">-WhatIf</span></span>
<span data-ttu-id="03bd1-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="03bd1-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03bd1-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03bd1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03bd1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03bd1-124">CommonParameters</span></span>
<span data-ttu-id="03bd1-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03bd1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03bd1-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="03bd1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03bd1-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03bd1-127">INPUTS</span></span>

### <span data-ttu-id="03bd1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="03bd1-128">System.String</span></span>

## <span data-ttu-id="03bd1-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03bd1-129">OUTPUTS</span></span>

### <span data-ttu-id="03bd1-130">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="03bd1-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="03bd1-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03bd1-131">NOTES</span></span>

## <span data-ttu-id="03bd1-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03bd1-132">RELATED LINKS</span></span>
