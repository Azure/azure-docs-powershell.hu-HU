---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: fa8c7768f2fcea53157f1b7bb3d89a5567ecdf2a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359224"
---
# <span data-ttu-id="a61c6-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="a61c6-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="a61c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a61c6-102">SYNOPSIS</span></span>
<span data-ttu-id="a61c6-103">Naplóprofilt kap.</span><span class="sxs-lookup"><span data-stu-id="a61c6-103">Gets a log profile.</span></span>

## <span data-ttu-id="a61c6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a61c6-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a61c6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a61c6-105">DESCRIPTION</span></span>
<span data-ttu-id="a61c6-106">A **Get-AzLogProfile** parancsmag naplóprofilt kap.</span><span class="sxs-lookup"><span data-stu-id="a61c6-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="a61c6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a61c6-107">EXAMPLES</span></span>

## <span data-ttu-id="a61c6-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a61c6-108">PARAMETERS</span></span>

### <span data-ttu-id="a61c6-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a61c6-109">-DefaultProfile</span></span>
<span data-ttu-id="a61c6-110">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a61c6-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a61c6-111">-Name</span><span class="sxs-lookup"><span data-stu-id="a61c6-111">-Name</span></span>
<span data-ttu-id="a61c6-112">A lekért naplóprofil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a61c6-112">Specifies the name of the log profile to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a61c6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a61c6-113">CommonParameters</span></span>
<span data-ttu-id="a61c6-114">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a61c6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a61c6-115">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a61c6-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a61c6-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a61c6-116">INPUTS</span></span>

### <span data-ttu-id="a61c6-117">System.String</span><span class="sxs-lookup"><span data-stu-id="a61c6-117">System.String</span></span>

## <span data-ttu-id="a61c6-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a61c6-118">OUTPUTS</span></span>

### <span data-ttu-id="a61c6-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="a61c6-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="a61c6-120">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a61c6-120">NOTES</span></span>

## <span data-ttu-id="a61c6-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a61c6-121">RELATED LINKS</span></span>

[<span data-ttu-id="a61c6-122">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="a61c6-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="a61c6-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="a61c6-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


