---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
ms.openlocfilehash: a01aeaa5868ece4f376dd5be934ba1029379958b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147483"
---
# <span data-ttu-id="8e2c1-101">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="8e2c1-101">Get-AzMediaServiceKey</span></span>

## <span data-ttu-id="8e2c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e2c1-102">SYNOPSIS</span></span>
<span data-ttu-id="8e2c1-103">A médiaszolgáltatással társított REST-végpont elérésének fő adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8e2c1-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="8e2c1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8e2c1-104">SYNTAX</span></span>

```
Get-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e2c1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8e2c1-105">DESCRIPTION</span></span>
<span data-ttu-id="8e2c1-106">A **Get-AzMediaServiceKey** parancsmag fontos információkat kap az Azure médiaszolgáltatáshoz társított REST-végpont eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="8e2c1-106">The **Get-AzMediaServiceKey** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="8e2c1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8e2c1-107">EXAMPLES</span></span>

### <span data-ttu-id="8e2c1-108">1. példa: A médiaszolgáltatás eléréséhez szükséges legfontosabb információk lekérte</span><span class="sxs-lookup"><span data-stu-id="8e2c1-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzMediaServiceKey -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="8e2c1-109">Ez a parancs az ResourceGroup0001 nevű erőforráscsoport MediaService001 nevű médiaszolgáltatásának eléréséhez szükséges legfontosabb információkat kapja.</span><span class="sxs-lookup"><span data-stu-id="8e2c1-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="8e2c1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e2c1-110">PARAMETERS</span></span>

### <span data-ttu-id="8e2c1-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8e2c1-111">-AccountName</span></span>
<span data-ttu-id="8e2c1-112">Annak a médiaszolgáltatásnak a nevét adja meg, amelyből a parancsmag a médiaszolgáltatás kulcsait kapja.</span><span class="sxs-lookup"><span data-stu-id="8e2c1-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

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

### <span data-ttu-id="8e2c1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e2c1-113">-DefaultProfile</span></span>
<span data-ttu-id="8e2c1-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8e2c1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e2c1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e2c1-115">-ResourceGroupName</span></span>
<span data-ttu-id="8e2c1-116">Annak az erőforráscsoportnak a nevét adja meg, amely az médiaszolgáltatást tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8e2c1-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="8e2c1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e2c1-117">CommonParameters</span></span>
<span data-ttu-id="8e2c1-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e2c1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e2c1-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e2c1-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e2c1-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e2c1-120">INPUTS</span></span>

### <span data-ttu-id="8e2c1-121">System.String</span><span class="sxs-lookup"><span data-stu-id="8e2c1-121">System.String</span></span>

## <span data-ttu-id="8e2c1-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e2c1-122">OUTPUTS</span></span>

### <span data-ttu-id="8e2c1-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="8e2c1-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="8e2c1-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8e2c1-124">NOTES</span></span>

## <span data-ttu-id="8e2c1-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e2c1-125">RELATED LINKS</span></span>

[<span data-ttu-id="8e2c1-126">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="8e2c1-126">Set-AzMediaServiceKey</span></span>](./Set-AzMediaServiceKey.md)


