---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: 8ad5026f0e033c6ab5825c9c862b19ad51b40ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835073"
---
# <span data-ttu-id="bb427-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="bb427-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="bb427-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bb427-102">SYNOPSIS</span></span>
<span data-ttu-id="bb427-103">Log-profilt kap.</span><span class="sxs-lookup"><span data-stu-id="bb427-103">Gets a log profile.</span></span>

## <span data-ttu-id="bb427-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bb427-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb427-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bb427-105">DESCRIPTION</span></span>
<span data-ttu-id="bb427-106">A **Get-AzLogProfile** parancsmag naplózási profilt kap.</span><span class="sxs-lookup"><span data-stu-id="bb427-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="bb427-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bb427-107">EXAMPLES</span></span>

## <span data-ttu-id="bb427-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bb427-108">PARAMETERS</span></span>

### <span data-ttu-id="bb427-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb427-109">-DefaultProfile</span></span>
<span data-ttu-id="bb427-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bb427-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb427-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bb427-111">-Name</span></span>
<span data-ttu-id="bb427-112">A beolvasott log-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb427-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="bb427-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb427-113">CommonParameters</span></span>
<span data-ttu-id="bb427-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bb427-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb427-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb427-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb427-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb427-116">INPUTS</span></span>

### <span data-ttu-id="bb427-117">System. String</span><span class="sxs-lookup"><span data-stu-id="bb427-117">System.String</span></span>

## <span data-ttu-id="bb427-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb427-118">OUTPUTS</span></span>

### <span data-ttu-id="bb427-119">Microsoft. Azure. commands. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="bb427-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="bb427-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bb427-120">NOTES</span></span>

## <span data-ttu-id="bb427-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb427-121">RELATED LINKS</span></span>

[<span data-ttu-id="bb427-122">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="bb427-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="bb427-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="bb427-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


