---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/test-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: a6e147d64a1dea77febc833b5c46e78d070f3ba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493144"
---
# <span data-ttu-id="f9e9f-101">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f9e9f-101">Test-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="f9e9f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f9e9f-102">SYNOPSIS</span></span>
<span data-ttu-id="f9e9f-103">Ellenőrzi, hogy létezik-e az adattó-alapú Analytics-fiók.</span><span class="sxs-lookup"><span data-stu-id="f9e9f-103">Checks for the existence of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9e9f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f9e9f-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9e9f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f9e9f-105">DESCRIPTION</span></span>
<span data-ttu-id="f9e9f-106">A **teszt-AzureRmDataLakeAnalyticsAccount** parancsmag ellenőrzi az adattó-alapú adatkezelési fiók létezését.</span><span class="sxs-lookup"><span data-stu-id="f9e9f-106">The **Test-AzureRmDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="f9e9f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f9e9f-107">EXAMPLES</span></span>

### <span data-ttu-id="f9e9f-108">1. példa: annak ellenőrzése, hogy létezik-e fiók</span><span class="sxs-lookup"><span data-stu-id="f9e9f-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="f9e9f-109">Ez a parancs azt teszteli, hogy a ContosoAdlAccount nevű fiók létezik-e.</span><span class="sxs-lookup"><span data-stu-id="f9e9f-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="f9e9f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f9e9f-110">PARAMETERS</span></span>

### <span data-ttu-id="f9e9f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9e9f-111">-DefaultProfile</span></span>
<span data-ttu-id="f9e9f-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f9e9f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9e9f-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f9e9f-113">-Name</span></span>
<span data-ttu-id="f9e9f-114">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9e9f-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9e9f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9e9f-115">-ResourceGroupName</span></span>
<span data-ttu-id="f9e9f-116">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9e9f-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9e9f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9e9f-117">CommonParameters</span></span>
<span data-ttu-id="f9e9f-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f9e9f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9e9f-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9e9f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9e9f-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9e9f-120">INPUTS</span></span>

### <span data-ttu-id="f9e9f-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="f9e9f-121">None</span></span>
<span data-ttu-id="f9e9f-122">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="f9e9f-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f9e9f-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9e9f-123">OUTPUTS</span></span>

### <span data-ttu-id="f9e9f-124">bool</span><span class="sxs-lookup"><span data-stu-id="f9e9f-124">bool</span></span>
<span data-ttu-id="f9e9f-125">Igaz vagy hamis: azt jelzi, hogy a fiók létezik-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="f9e9f-125">True or false indicating whether the account exists or not.</span></span>

## <span data-ttu-id="f9e9f-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f9e9f-126">NOTES</span></span>

## <span data-ttu-id="f9e9f-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9e9f-127">RELATED LINKS</span></span>

[<span data-ttu-id="f9e9f-128">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f9e9f-128">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f9e9f-129">Új – AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f9e9f-129">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f9e9f-130">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f9e9f-130">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)


