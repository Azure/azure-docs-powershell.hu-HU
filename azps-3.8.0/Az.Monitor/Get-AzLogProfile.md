---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: fa8c7768f2fcea53157f1b7bb3d89a5567ecdf2a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014512"
---
# <span data-ttu-id="ece71-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="ece71-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="ece71-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ece71-102">SYNOPSIS</span></span>
<span data-ttu-id="ece71-103">Log-profilt kap.</span><span class="sxs-lookup"><span data-stu-id="ece71-103">Gets a log profile.</span></span>

## <span data-ttu-id="ece71-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ece71-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ece71-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ece71-105">DESCRIPTION</span></span>
<span data-ttu-id="ece71-106">A **Get-AzLogProfile** parancsmag naplózási profilt kap.</span><span class="sxs-lookup"><span data-stu-id="ece71-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="ece71-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ece71-107">EXAMPLES</span></span>

## <span data-ttu-id="ece71-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ece71-108">PARAMETERS</span></span>

### <span data-ttu-id="ece71-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece71-109">-DefaultProfile</span></span>
<span data-ttu-id="ece71-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ece71-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ece71-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ece71-111">-Name</span></span>
<span data-ttu-id="ece71-112">A beolvasott log-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ece71-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="ece71-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece71-113">CommonParameters</span></span>
<span data-ttu-id="ece71-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ece71-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece71-115">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ece71-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece71-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ece71-116">INPUTS</span></span>

### <span data-ttu-id="ece71-117">System. String</span><span class="sxs-lookup"><span data-stu-id="ece71-117">System.String</span></span>

## <span data-ttu-id="ece71-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ece71-118">OUTPUTS</span></span>

### <span data-ttu-id="ece71-119">Microsoft. Azure. commands. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="ece71-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="ece71-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ece71-120">NOTES</span></span>

## <span data-ttu-id="ece71-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ece71-121">RELATED LINKS</span></span>

[<span data-ttu-id="ece71-122">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="ece71-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="ece71-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="ece71-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


