---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1ab8cbd8ead120ecc531e3e252fe2c31a58f10c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672224"
---
# <span data-ttu-id="a8c24-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a8c24-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="a8c24-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8c24-102">SYNOPSIS</span></span>
<span data-ttu-id="a8c24-103">Információt kap az adattó Analytics-fiókjáról.</span><span class="sxs-lookup"><span data-stu-id="a8c24-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8c24-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8c24-104">SYNTAX</span></span>

### <span data-ttu-id="a8c24-105">All in előfizetés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a8c24-105">All In Subscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8c24-106">Minden az erőforrás csoportban</span><span class="sxs-lookup"><span data-stu-id="a8c24-106">All In Resource Group</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8c24-107">Konkrét fiók</span><span class="sxs-lookup"><span data-stu-id="a8c24-107">Specific Account</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8c24-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8c24-108">DESCRIPTION</span></span>
<span data-ttu-id="a8c24-109">A **Get-AzureRmDataLakeAnalyticsAccount** parancsmag információkat kap az Azure-alapú adattó Analytics-fiókjáról.</span><span class="sxs-lookup"><span data-stu-id="a8c24-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="a8c24-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a8c24-110">EXAMPLES</span></span>

### <span data-ttu-id="a8c24-111">1. példa: adatok beolvasása az adattó Analytics-fiókjával</span><span class="sxs-lookup"><span data-stu-id="a8c24-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="a8c24-112">Ez a parancs információkat kap a ContosoAdlAccount nevű fiókról.</span><span class="sxs-lookup"><span data-stu-id="a8c24-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="a8c24-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8c24-113">PARAMETERS</span></span>

### <span data-ttu-id="a8c24-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a8c24-114">-Name</span></span>
<span data-ttu-id="a8c24-115">Az adattó-Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8c24-115">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8c24-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8c24-116">-ResourceGroupName</span></span>
<span data-ttu-id="a8c24-117">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8c24-117">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8c24-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8c24-118">-DefaultProfile</span></span>
<span data-ttu-id="a8c24-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8c24-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c24-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8c24-120">CommonParameters</span></span>
<span data-ttu-id="a8c24-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8c24-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8c24-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8c24-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8c24-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8c24-123">INPUTS</span></span>

## <span data-ttu-id="a8c24-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8c24-124">OUTPUTS</span></span>

### <span data-ttu-id="a8c24-125">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a8c24-125">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="a8c24-126">A megadott fiók adatai.</span><span class="sxs-lookup"><span data-stu-id="a8c24-126">The specified account details.</span></span>

### <span data-ttu-id="a8c24-127">Lista<PSDataLakeAnalyticsAccount></span><span class="sxs-lookup"><span data-stu-id="a8c24-127">List<PSDataLakeAnalyticsAccount></span></span>
<span data-ttu-id="a8c24-128">A megadott erőforráscsoport vagy-előfizetés fiókjainak listája.</span><span class="sxs-lookup"><span data-stu-id="a8c24-128">The list of accounts in the specified resource group or subscription.</span></span>

## <span data-ttu-id="a8c24-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8c24-129">NOTES</span></span>

## <span data-ttu-id="a8c24-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8c24-130">RELATED LINKS</span></span>

[<span data-ttu-id="a8c24-131">Új – AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a8c24-131">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a8c24-132">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a8c24-132">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a8c24-133">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a8c24-133">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a8c24-134">Teszt-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a8c24-134">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


