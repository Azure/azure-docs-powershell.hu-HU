---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: f15ef7201622394a2b96964244980b059f1222c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491954"
---
# <span data-ttu-id="76abe-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="76abe-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="76abe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76abe-102">SYNOPSIS</span></span>
<span data-ttu-id="76abe-103">Adatokat kap az adattó áruházbeli fiókról.</span><span class="sxs-lookup"><span data-stu-id="76abe-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76abe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76abe-104">SYNTAX</span></span>

### <span data-ttu-id="76abe-105">GetAllInSubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="76abe-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76abe-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="76abe-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="76abe-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="76abe-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76abe-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="76abe-108">DESCRIPTION</span></span>
<span data-ttu-id="76abe-109">A **Get-AzureRmDataLakeStoreAccount** parancsmag az adattó-tároló fiók adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="76abe-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="76abe-110">Példák</span><span class="sxs-lookup"><span data-stu-id="76abe-110">EXAMPLES</span></span>

### <span data-ttu-id="76abe-111">Példa 1: adattó áruházbeli fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="76abe-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="76abe-112">Ez a parancs a ContosoADL nevű fiókot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="76abe-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="76abe-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76abe-113">PARAMETERS</span></span>

### <span data-ttu-id="76abe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76abe-114">-DefaultProfile</span></span>
<span data-ttu-id="76abe-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="76abe-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76abe-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="76abe-116">-Name</span></span>
<span data-ttu-id="76abe-117">A beolvasott fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76abe-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="76abe-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76abe-118">-ResourceGroupName</span></span>
<span data-ttu-id="76abe-119">Az adattó-tároló fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76abe-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="76abe-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76abe-120">CommonParameters</span></span>
<span data-ttu-id="76abe-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76abe-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76abe-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76abe-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76abe-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76abe-123">INPUTS</span></span>

### <span data-ttu-id="76abe-124">System. String</span><span class="sxs-lookup"><span data-stu-id="76abe-124">System.String</span></span>

## <span data-ttu-id="76abe-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76abe-125">OUTPUTS</span></span>

### <span data-ttu-id="76abe-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="76abe-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="76abe-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76abe-127">NOTES</span></span>

## <span data-ttu-id="76abe-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76abe-128">RELATED LINKS</span></span>

[<span data-ttu-id="76abe-129">Új – AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="76abe-129">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="76abe-130">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="76abe-130">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="76abe-131">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="76abe-131">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="76abe-132">Teszt-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="76abe-132">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


