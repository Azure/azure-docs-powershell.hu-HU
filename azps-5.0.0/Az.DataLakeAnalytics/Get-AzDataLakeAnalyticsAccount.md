---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1894e5a79660558163d9b95ce49f1736ea002bf9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298130"
---
# <span data-ttu-id="fddaa-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="fddaa-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="fddaa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fddaa-102">SYNOPSIS</span></span>
<span data-ttu-id="fddaa-103">Információt kap az adattó Analytics-fiókjáról.</span><span class="sxs-lookup"><span data-stu-id="fddaa-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="fddaa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fddaa-104">SYNTAX</span></span>

### <span data-ttu-id="fddaa-105">GetAllInSubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fddaa-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fddaa-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fddaa-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fddaa-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="fddaa-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fddaa-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fddaa-108">DESCRIPTION</span></span>
<span data-ttu-id="fddaa-109">A **Get-AzDataLakeAnalyticsAccount** parancsmag információkat kap az Azure-alapú adattó Analytics-fiókjáról.</span><span class="sxs-lookup"><span data-stu-id="fddaa-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="fddaa-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fddaa-110">EXAMPLES</span></span>

### <span data-ttu-id="fddaa-111">1. példa: adatok beolvasása az adattó Analytics-fiókjával</span><span class="sxs-lookup"><span data-stu-id="fddaa-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="fddaa-112">Ez a parancs információkat kap a ContosoAdlAccount nevű fiókról.</span><span class="sxs-lookup"><span data-stu-id="fddaa-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="fddaa-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fddaa-113">PARAMETERS</span></span>

### <span data-ttu-id="fddaa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fddaa-114">-DefaultProfile</span></span>
<span data-ttu-id="fddaa-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fddaa-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fddaa-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fddaa-116">-Name</span></span>
<span data-ttu-id="fddaa-117">Az adattó-Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fddaa-117">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fddaa-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fddaa-118">-ResourceGroupName</span></span>
<span data-ttu-id="fddaa-119">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fddaa-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fddaa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fddaa-120">CommonParameters</span></span>
<span data-ttu-id="fddaa-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fddaa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fddaa-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fddaa-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fddaa-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fddaa-123">INPUTS</span></span>

### <span data-ttu-id="fddaa-124">System. String</span><span class="sxs-lookup"><span data-stu-id="fddaa-124">System.String</span></span>

## <span data-ttu-id="fddaa-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fddaa-125">OUTPUTS</span></span>

### <span data-ttu-id="fddaa-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="fddaa-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="fddaa-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="fddaa-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="fddaa-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fddaa-128">NOTES</span></span>

## <span data-ttu-id="fddaa-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fddaa-129">RELATED LINKS</span></span>

[<span data-ttu-id="fddaa-130">Új – AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="fddaa-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="fddaa-131">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="fddaa-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="fddaa-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="fddaa-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="fddaa-133">Teszt-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="fddaa-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


