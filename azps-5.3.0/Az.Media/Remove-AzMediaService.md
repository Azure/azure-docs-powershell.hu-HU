---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: 525c5e2bfd15811e861945a6404e0b88274e2563
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481265"
---
# <span data-ttu-id="cce8f-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="cce8f-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="cce8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cce8f-102">SYNOPSIS</span></span>
<span data-ttu-id="cce8f-103">Eltávolít egy médiaszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="cce8f-103">Removes a media service.</span></span>

## <span data-ttu-id="cce8f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cce8f-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cce8f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cce8f-105">DESCRIPTION</span></span>
<span data-ttu-id="cce8f-106">A **Remove-AzMediaService** parancsmag eltávolít egy médiaszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="cce8f-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="cce8f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cce8f-107">EXAMPLES</span></span>

### <span data-ttu-id="cce8f-108">1. példa: Médiaszolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="cce8f-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="cce8f-109">Ez a parancs eltávolítja a MediaService0011 nevű médiaszolgáltatást az ResourceGroup0001 nevű erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="cce8f-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="cce8f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cce8f-110">PARAMETERS</span></span>

### <span data-ttu-id="cce8f-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cce8f-111">-AccountName</span></span>
<span data-ttu-id="cce8f-112">Annak a médiaszolgáltatásnak a neve, amelyről a parancsmag eltávolítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cce8f-112">Specifies the name of the media service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cce8f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cce8f-113">-DefaultProfile</span></span>
<span data-ttu-id="cce8f-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cce8f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cce8f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cce8f-115">-Force</span></span>
<span data-ttu-id="cce8f-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="cce8f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cce8f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cce8f-117">-ResourceGroupName</span></span>
<span data-ttu-id="cce8f-118">Annak az erőforráscsoportnak a nevét adja meg, amely az médiaszolgáltatást tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="cce8f-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="cce8f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cce8f-119">-Confirm</span></span>
<span data-ttu-id="cce8f-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cce8f-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cce8f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cce8f-121">-WhatIf</span></span>
<span data-ttu-id="cce8f-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cce8f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cce8f-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cce8f-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cce8f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cce8f-124">CommonParameters</span></span>
<span data-ttu-id="cce8f-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cce8f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cce8f-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cce8f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cce8f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cce8f-127">INPUTS</span></span>

### <span data-ttu-id="cce8f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="cce8f-128">System.String</span></span>

## <span data-ttu-id="cce8f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cce8f-129">OUTPUTS</span></span>

### <span data-ttu-id="cce8f-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cce8f-130">System.Boolean</span></span>

## <span data-ttu-id="cce8f-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cce8f-131">NOTES</span></span>

## <span data-ttu-id="cce8f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cce8f-132">RELATED LINKS</span></span>

[<span data-ttu-id="cce8f-133">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="cce8f-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="cce8f-134">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="cce8f-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="cce8f-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="cce8f-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


