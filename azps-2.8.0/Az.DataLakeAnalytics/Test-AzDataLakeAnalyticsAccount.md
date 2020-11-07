---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 77247853fe6412b0d01fb01c71e592efca12063d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666883"
---
# <span data-ttu-id="5bcc1-101">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5bcc1-101">Test-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="5bcc1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5bcc1-102">SYNOPSIS</span></span>
<span data-ttu-id="5bcc1-103">Ellenőrzi, hogy létezik-e az adattó-alapú Analytics-fiók.</span><span class="sxs-lookup"><span data-stu-id="5bcc1-103">Checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="5bcc1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5bcc1-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bcc1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5bcc1-105">DESCRIPTION</span></span>
<span data-ttu-id="5bcc1-106">A **teszt-AzDataLakeAnalyticsAccount** parancsmag ellenőrzi az adattó-alapú adatkezelési fiók létezését.</span><span class="sxs-lookup"><span data-stu-id="5bcc1-106">The **Test-AzDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="5bcc1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5bcc1-107">EXAMPLES</span></span>

### <span data-ttu-id="5bcc1-108">1. példa: annak ellenőrzése, hogy létezik-e fiók</span><span class="sxs-lookup"><span data-stu-id="5bcc1-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="5bcc1-109">Ez a parancs azt teszteli, hogy a ContosoAdlAccount nevű fiók létezik-e.</span><span class="sxs-lookup"><span data-stu-id="5bcc1-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="5bcc1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5bcc1-110">PARAMETERS</span></span>

### <span data-ttu-id="5bcc1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bcc1-111">-DefaultProfile</span></span>
<span data-ttu-id="5bcc1-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5bcc1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bcc1-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5bcc1-113">-Name</span></span>
<span data-ttu-id="5bcc1-114">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bcc1-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="5bcc1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bcc1-115">-ResourceGroupName</span></span>
<span data-ttu-id="5bcc1-116">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bcc1-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="5bcc1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bcc1-117">CommonParameters</span></span>
<span data-ttu-id="5bcc1-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5bcc1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bcc1-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bcc1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bcc1-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bcc1-120">INPUTS</span></span>

### <span data-ttu-id="5bcc1-121">System. String</span><span class="sxs-lookup"><span data-stu-id="5bcc1-121">System.String</span></span>

## <span data-ttu-id="5bcc1-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bcc1-122">OUTPUTS</span></span>

### <span data-ttu-id="5bcc1-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5bcc1-123">System.Boolean</span></span>

## <span data-ttu-id="5bcc1-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5bcc1-124">NOTES</span></span>

## <span data-ttu-id="5bcc1-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5bcc1-125">RELATED LINKS</span></span>

[<span data-ttu-id="5bcc1-126">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5bcc1-126">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="5bcc1-127">Új – AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5bcc1-127">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="5bcc1-128">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5bcc1-128">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)


