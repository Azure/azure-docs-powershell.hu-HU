---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: b5c1303625676006929a3c2eee80f5d5961bc438
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009158"
---
# <span data-ttu-id="0a6fc-101">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0a6fc-101">Test-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="0a6fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a6fc-102">SYNOPSIS</span></span>
<span data-ttu-id="0a6fc-103">Ellenőrzi, hogy létezik-e Data Lake Analytics-fiók.</span><span class="sxs-lookup"><span data-stu-id="0a6fc-103">Checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="0a6fc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0a6fc-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a6fc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0a6fc-105">DESCRIPTION</span></span>
<span data-ttu-id="0a6fc-106">A **Test-AzDataLakeAnalyticsAccount** parancsmag ellenőrzi, hogy létezik-e Data Lake Analytics-fiók.</span><span class="sxs-lookup"><span data-stu-id="0a6fc-106">The **Test-AzDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="0a6fc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0a6fc-107">EXAMPLES</span></span>

### <span data-ttu-id="0a6fc-108">1. példa: Fiók létezik-e?</span><span class="sxs-lookup"><span data-stu-id="0a6fc-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="0a6fc-109">Ez a parancs teszteli, hogy létezik-e a ContosoAdlAccount nevű fiók.</span><span class="sxs-lookup"><span data-stu-id="0a6fc-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="0a6fc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a6fc-110">PARAMETERS</span></span>

### <span data-ttu-id="0a6fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a6fc-111">-DefaultProfile</span></span>
<span data-ttu-id="0a6fc-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0a6fc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a6fc-113">-Name</span><span class="sxs-lookup"><span data-stu-id="0a6fc-113">-Name</span></span>
<span data-ttu-id="0a6fc-114">A Data Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a6fc-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="0a6fc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a6fc-115">-ResourceGroupName</span></span>
<span data-ttu-id="0a6fc-116">A Data Lake Analytics-fiók erőforráscsoportnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a6fc-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6fc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a6fc-117">CommonParameters</span></span>
<span data-ttu-id="0a6fc-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a6fc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a6fc-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a6fc-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a6fc-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a6fc-120">INPUTS</span></span>

### <span data-ttu-id="0a6fc-121">System.String</span><span class="sxs-lookup"><span data-stu-id="0a6fc-121">System.String</span></span>

## <span data-ttu-id="0a6fc-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a6fc-122">OUTPUTS</span></span>

### <span data-ttu-id="0a6fc-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0a6fc-123">System.Boolean</span></span>

## <span data-ttu-id="0a6fc-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0a6fc-124">NOTES</span></span>

## <span data-ttu-id="0a6fc-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a6fc-125">RELATED LINKS</span></span>

[<span data-ttu-id="0a6fc-126">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0a6fc-126">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0a6fc-127">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0a6fc-127">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0a6fc-128">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0a6fc-128">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)


