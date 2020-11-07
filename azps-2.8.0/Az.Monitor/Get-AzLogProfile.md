---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: 1f7306d78d7c0405929ba7dae2512b141a4f4a89
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665850"
---
# <span data-ttu-id="e4239-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="e4239-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="e4239-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4239-102">SYNOPSIS</span></span>
<span data-ttu-id="e4239-103">Log-profilt kap.</span><span class="sxs-lookup"><span data-stu-id="e4239-103">Gets a log profile.</span></span>

## <span data-ttu-id="e4239-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4239-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4239-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4239-105">DESCRIPTION</span></span>
<span data-ttu-id="e4239-106">A **Get-AzLogProfile** parancsmag naplózási profilt kap.</span><span class="sxs-lookup"><span data-stu-id="e4239-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="e4239-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e4239-107">EXAMPLES</span></span>

## <span data-ttu-id="e4239-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4239-108">PARAMETERS</span></span>

### <span data-ttu-id="e4239-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4239-109">-DefaultProfile</span></span>
<span data-ttu-id="e4239-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e4239-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4239-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e4239-111">-Name</span></span>
<span data-ttu-id="e4239-112">A beolvasott log-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4239-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="e4239-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4239-113">CommonParameters</span></span>
<span data-ttu-id="e4239-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4239-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4239-115">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e4239-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4239-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4239-116">INPUTS</span></span>

### <span data-ttu-id="e4239-117">System. String</span><span class="sxs-lookup"><span data-stu-id="e4239-117">System.String</span></span>

## <span data-ttu-id="e4239-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4239-118">OUTPUTS</span></span>

### <span data-ttu-id="e4239-119">Microsoft. Azure. commands. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="e4239-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="e4239-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4239-120">NOTES</span></span>

## <span data-ttu-id="e4239-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4239-121">RELATED LINKS</span></span>

[<span data-ttu-id="e4239-122">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="e4239-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="e4239-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="e4239-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


