---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: b06b64b81679d1f0f9429be0362f936046e54ee5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836325"
---
# <span data-ttu-id="86411-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="86411-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="86411-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86411-102">SYNOPSIS</span></span>
<span data-ttu-id="86411-103">Adatokat kap az adattó áruházbeli fiókról.</span><span class="sxs-lookup"><span data-stu-id="86411-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="86411-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86411-104">SYNTAX</span></span>

### <span data-ttu-id="86411-105">GetAllInSubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86411-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86411-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="86411-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86411-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="86411-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86411-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="86411-108">DESCRIPTION</span></span>
<span data-ttu-id="86411-109">A **Get-AzDataLakeStoreAccount** parancsmag az adattó-tároló fiók adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="86411-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="86411-110">Példák</span><span class="sxs-lookup"><span data-stu-id="86411-110">EXAMPLES</span></span>

### <span data-ttu-id="86411-111">Példa 1: adattó áruházbeli fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="86411-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="86411-112">Ez a parancs a ContosoADL nevű fiókot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="86411-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="86411-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86411-113">PARAMETERS</span></span>

### <span data-ttu-id="86411-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86411-114">-DefaultProfile</span></span>
<span data-ttu-id="86411-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="86411-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86411-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="86411-116">-Name</span></span>
<span data-ttu-id="86411-117">A beolvasott fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="86411-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="86411-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86411-118">-ResourceGroupName</span></span>
<span data-ttu-id="86411-119">Az adattó-tároló fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="86411-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="86411-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86411-120">CommonParameters</span></span>
<span data-ttu-id="86411-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86411-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86411-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86411-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86411-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86411-123">INPUTS</span></span>

### <span data-ttu-id="86411-124">System. String</span><span class="sxs-lookup"><span data-stu-id="86411-124">System.String</span></span>

## <span data-ttu-id="86411-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86411-125">OUTPUTS</span></span>

### <span data-ttu-id="86411-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="86411-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="86411-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86411-127">NOTES</span></span>

## <span data-ttu-id="86411-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86411-128">RELATED LINKS</span></span>

[<span data-ttu-id="86411-129">Új – AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="86411-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="86411-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="86411-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="86411-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="86411-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="86411-132">Teszt-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="86411-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


