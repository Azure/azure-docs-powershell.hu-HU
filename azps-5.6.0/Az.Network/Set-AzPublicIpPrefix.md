---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: 2937aafbcffd2444051b9bed0a764cb3aede6c52
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001046"
---
# <span data-ttu-id="53b38-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53b38-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="53b38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53b38-102">SYNOPSIS</span></span>
<span data-ttu-id="53b38-103">Egy meglévő PublicIpPrefix címkéit állítja be</span><span class="sxs-lookup"><span data-stu-id="53b38-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="53b38-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="53b38-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53b38-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="53b38-105">DESCRIPTION</span></span>
<span data-ttu-id="53b38-106">A **Set-AzPublicIpPrefix** parancsmag beállítja egy nyilvános IP-előtag címkéit.</span><span class="sxs-lookup"><span data-stu-id="53b38-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="53b38-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="53b38-107">EXAMPLES</span></span>

### <span data-ttu-id="53b38-108">Nyilvános IP-előtag címkéinek beállítása</span><span class="sxs-lookup"><span data-stu-id="53b38-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="53b38-109">Az első parancs egy meglévő nyilvános IP-előtagot kap, a második beállítja a Címkék tulajdonságot, a harmadik pedig frissíti a meglévő objektumot.</span><span class="sxs-lookup"><span data-stu-id="53b38-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="53b38-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53b38-110">PARAMETERS</span></span>

### <span data-ttu-id="53b38-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53b38-111">-AsJob</span></span>
<span data-ttu-id="53b38-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="53b38-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53b38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53b38-113">-DefaultProfile</span></span>
<span data-ttu-id="53b38-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53b38-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53b38-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53b38-115">-PublicIpPrefix</span></span>
<span data-ttu-id="53b38-116">The PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53b38-116">The PublicIpPrefix</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53b38-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53b38-117">-Confirm</span></span>
<span data-ttu-id="53b38-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="53b38-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53b38-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53b38-119">-WhatIf</span></span>
<span data-ttu-id="53b38-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="53b38-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53b38-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="53b38-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53b38-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53b38-122">CommonParameters</span></span>
<span data-ttu-id="53b38-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53b38-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53b38-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53b38-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53b38-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53b38-125">INPUTS</span></span>

### <span data-ttu-id="53b38-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53b38-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="53b38-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53b38-127">OUTPUTS</span></span>

### <span data-ttu-id="53b38-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53b38-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="53b38-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="53b38-129">NOTES</span></span>

## <span data-ttu-id="53b38-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53b38-130">RELATED LINKS</span></span>

[<span data-ttu-id="53b38-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53b38-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="53b38-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53b38-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="53b38-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53b38-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)
