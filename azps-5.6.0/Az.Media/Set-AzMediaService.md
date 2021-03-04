---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/powershell/module/az.media/set-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
ms.openlocfilehash: 410b1c87832b4debdfd50cbe6adf27326f12a303
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934113"
---
# <span data-ttu-id="5ab45-101">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="5ab45-101">Set-AzMediaService</span></span>

## <span data-ttu-id="5ab45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ab45-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab45-103">Módosítja egy meglévő médiaszolgáltatás megadott tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="5ab45-103">Modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="5ab45-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5ab45-104">SYNTAX</span></span>

```
Set-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ab45-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5ab45-105">DESCRIPTION</span></span>
<span data-ttu-id="5ab45-106">A **Set-AzMediaService** parancsmag módosítja egy meglévő médiaszolgáltatás megadott tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="5ab45-106">The **Set-AzMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="5ab45-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5ab45-107">EXAMPLES</span></span>

### <span data-ttu-id="5ab45-108">1. példa: Meglévő médiaszolgáltatás módosítása</span><span class="sxs-lookup"><span data-stu-id="5ab45-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tag $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="5ab45-109">Az első parancs címkék sorozatát hozza létre, és ezeket a címkéket a $Tags.</span><span class="sxs-lookup"><span data-stu-id="5ab45-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>
<span data-ttu-id="5ab45-110">Ez a második parancs frissíti a MediaService001 nevű médiaszolgáltatást, amely az ResourceGroup123 nevű erőforráscsoporthoz tartozik egy változóban tárolt $Tags címkével.</span><span class="sxs-lookup"><span data-stu-id="5ab45-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="5ab45-111">A parancs egy másik változóban tárolt tárolókonfigurációs objektumok $StorageAccounts is.</span><span class="sxs-lookup"><span data-stu-id="5ab45-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="5ab45-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ab45-112">PARAMETERS</span></span>

### <span data-ttu-id="5ab45-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5ab45-113">-AccountName</span></span>
<span data-ttu-id="5ab45-114">Annak a médiaszolgáltatásnak a nevét adja meg, amely módosítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5ab45-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5ab45-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab45-115">-DefaultProfile</span></span>
<span data-ttu-id="5ab45-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5ab45-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ab45-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ab45-117">-ResourceGroupName</span></span>
<span data-ttu-id="5ab45-118">Annak az erőforráscsoportnak a nevét adja meg, amely az médiaszolgáltatást tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="5ab45-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="5ab45-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="5ab45-119">-StorageAccounts</span></span>
<span data-ttu-id="5ab45-120">A parancsmag által az médiaszolgáltatáshoz társítandó tárfiókok tömbje.</span><span class="sxs-lookup"><span data-stu-id="5ab45-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ab45-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="5ab45-121">-Tag</span></span>
<span data-ttu-id="5ab45-122">A médiafiókhoz társított címkék.</span><span class="sxs-lookup"><span data-stu-id="5ab45-122">The tags associated with the media account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ab45-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ab45-123">-Confirm</span></span>
<span data-ttu-id="5ab45-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5ab45-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ab45-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ab45-125">-WhatIf</span></span>
<span data-ttu-id="5ab45-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5ab45-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ab45-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ab45-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ab45-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab45-128">CommonParameters</span></span>
<span data-ttu-id="5ab45-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ab45-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab45-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ab45-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab45-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ab45-131">INPUTS</span></span>

### <span data-ttu-id="5ab45-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5ab45-132">System.String</span></span>

### <span data-ttu-id="5ab45-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5ab45-133">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5ab45-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span><span class="sxs-lookup"><span data-stu-id="5ab45-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="5ab45-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ab45-135">OUTPUTS</span></span>

### <span data-ttu-id="5ab45-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="5ab45-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="5ab45-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5ab45-137">NOTES</span></span>

## <span data-ttu-id="5ab45-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ab45-138">RELATED LINKS</span></span>

[<span data-ttu-id="5ab45-139">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="5ab45-139">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="5ab45-140">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="5ab45-140">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="5ab45-141">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="5ab45-141">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)


