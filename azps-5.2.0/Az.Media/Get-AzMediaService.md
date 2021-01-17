---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: bd1f3f2d202e21f12ba7bd111853473094d042e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359251"
---
# <span data-ttu-id="bfd59-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="bfd59-101">Get-AzMediaService</span></span>

## <span data-ttu-id="bfd59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfd59-102">SYNOPSIS</span></span>
<span data-ttu-id="bfd59-103">Információkat kap egy médiaszolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="bfd59-103">Gets information about a media service.</span></span>

## <span data-ttu-id="bfd59-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bfd59-104">SYNTAX</span></span>

### <span data-ttu-id="bfd59-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfd59-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfd59-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfd59-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfd59-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bfd59-107">DESCRIPTION</span></span>
<span data-ttu-id="bfd59-108">A **Get-AzMediaService** parancsmag információt kap egy médiaszolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="bfd59-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="bfd59-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bfd59-109">EXAMPLES</span></span>

### <span data-ttu-id="bfd59-110">1. példa: Az erőforráscsoport összes médiaszolgáltatásának lekérte</span><span class="sxs-lookup"><span data-stu-id="bfd59-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="bfd59-111">Ez a parancs az Erőforráscsoport001 nevű erőforráscsoport összes médiaszolgáltatásának tulajdonságait beveszi.</span><span class="sxs-lookup"><span data-stu-id="bfd59-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="bfd59-112">2. példa: Médiaszolgáltatás tulajdonságainak lekérte</span><span class="sxs-lookup"><span data-stu-id="bfd59-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="bfd59-113">Ez a parancs a MediaService1 nevű médiaszolgáltatás tulajdonságait kapja meg, amely az ResourceGroup002 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="bfd59-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="bfd59-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfd59-114">PARAMETERS</span></span>

### <span data-ttu-id="bfd59-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bfd59-115">-AccountName</span></span>
<span data-ttu-id="bfd59-116">A parancsmag médiaszolgáltatásának a neve.</span><span class="sxs-lookup"><span data-stu-id="bfd59-116">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfd59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfd59-117">-DefaultProfile</span></span>
<span data-ttu-id="bfd59-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bfd59-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bfd59-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfd59-119">-ResourceGroupName</span></span>
<span data-ttu-id="bfd59-120">Annak az erőforráscsoportnak a nevét adja meg, amely az médiaszolgáltatást tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bfd59-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="bfd59-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfd59-121">CommonParameters</span></span>
<span data-ttu-id="bfd59-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfd59-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfd59-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfd59-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfd59-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bfd59-124">INPUTS</span></span>

### <span data-ttu-id="bfd59-125">System.String</span><span class="sxs-lookup"><span data-stu-id="bfd59-125">System.String</span></span>

## <span data-ttu-id="bfd59-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfd59-126">OUTPUTS</span></span>

### <span data-ttu-id="bfd59-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="bfd59-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="bfd59-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bfd59-128">NOTES</span></span>

## <span data-ttu-id="bfd59-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bfd59-129">RELATED LINKS</span></span>

[<span data-ttu-id="bfd59-130">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="bfd59-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="bfd59-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="bfd59-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="bfd59-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="bfd59-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


