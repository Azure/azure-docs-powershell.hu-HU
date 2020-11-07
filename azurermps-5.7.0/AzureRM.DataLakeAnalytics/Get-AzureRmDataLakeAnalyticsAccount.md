---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 71d524aeea441c80b90642a01f1a2f34996904ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672380"
---
# <span data-ttu-id="1240c-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1240c-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="1240c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1240c-102">SYNOPSIS</span></span>
<span data-ttu-id="1240c-103">Információt kap az adattó Analytics-fiókjáról.</span><span class="sxs-lookup"><span data-stu-id="1240c-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1240c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1240c-104">SYNTAX</span></span>

### <span data-ttu-id="1240c-105">GetAllInSubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1240c-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1240c-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1240c-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1240c-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="1240c-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1240c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1240c-108">DESCRIPTION</span></span>
<span data-ttu-id="1240c-109">A **Get-AzureRmDataLakeAnalyticsAccount** parancsmag információkat kap az Azure-alapú adattó Analytics-fiókjáról.</span><span class="sxs-lookup"><span data-stu-id="1240c-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="1240c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1240c-110">EXAMPLES</span></span>

### <span data-ttu-id="1240c-111">1. példa: adatok beolvasása az adattó Analytics-fiókjával</span><span class="sxs-lookup"><span data-stu-id="1240c-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="1240c-112">Ez a parancs információkat kap a ContosoAdlAccount nevű fiókról.</span><span class="sxs-lookup"><span data-stu-id="1240c-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="1240c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1240c-113">PARAMETERS</span></span>

### <span data-ttu-id="1240c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1240c-114">-DefaultProfile</span></span>
<span data-ttu-id="1240c-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1240c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1240c-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1240c-116">-Name</span></span>
<span data-ttu-id="1240c-117">Az adattó-Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1240c-117">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1240c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1240c-118">-ResourceGroupName</span></span>
<span data-ttu-id="1240c-119">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1240c-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1240c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1240c-120">CommonParameters</span></span>
<span data-ttu-id="1240c-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1240c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1240c-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1240c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1240c-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1240c-123">INPUTS</span></span>

### <span data-ttu-id="1240c-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="1240c-124">None</span></span>
<span data-ttu-id="1240c-125">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="1240c-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1240c-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1240c-126">OUTPUTS</span></span>

### <span data-ttu-id="1240c-127">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1240c-127">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="1240c-128">A megadott fiók adatai.</span><span class="sxs-lookup"><span data-stu-id="1240c-128">The specified account details.</span></span>

### <span data-ttu-id="1240c-129">Lista<PSDataLakeAnalyticsAccountBasic></span><span class="sxs-lookup"><span data-stu-id="1240c-129">List<PSDataLakeAnalyticsAccountBasic></span></span>
<span data-ttu-id="1240c-130">A megadott erőforráscsoport vagy-előfizetés fiókjainak listája.</span><span class="sxs-lookup"><span data-stu-id="1240c-130">The list of accounts in the specified resource group or subscription.</span></span>

## <span data-ttu-id="1240c-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1240c-131">NOTES</span></span>

## <span data-ttu-id="1240c-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1240c-132">RELATED LINKS</span></span>

[<span data-ttu-id="1240c-133">Új – AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1240c-133">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="1240c-134">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1240c-134">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="1240c-135">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1240c-135">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="1240c-136">Teszt-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1240c-136">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


