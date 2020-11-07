---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 5e62bc19ec400f3dbfff3c089880cd14ce95609e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666906"
---
# <span data-ttu-id="2ca38-101">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="2ca38-101">Remove-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="2ca38-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ca38-102">SYNOPSIS</span></span>
<span data-ttu-id="2ca38-103">Az adattó-Analytics-fiók törlése</span><span class="sxs-lookup"><span data-stu-id="2ca38-103">Deletes a Data Lake Analytics account.</span></span>

## <span data-ttu-id="2ca38-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ca38-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ca38-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ca38-105">DESCRIPTION</span></span>
<span data-ttu-id="2ca38-106">A **Remove-AzDataLakeAnalyticsAccount** parancsmag véglegesen törli az Azure Data Lake Analytics-fiókját.</span><span class="sxs-lookup"><span data-stu-id="2ca38-106">The **Remove-AzDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="2ca38-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2ca38-107">EXAMPLES</span></span>

### <span data-ttu-id="2ca38-108">1. példa: fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2ca38-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="2ca38-109">Ez a parancs eltávolítja a megadott Data Lake Analytics-fiókot.</span><span class="sxs-lookup"><span data-stu-id="2ca38-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="2ca38-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ca38-110">PARAMETERS</span></span>

### <span data-ttu-id="2ca38-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ca38-111">-DefaultProfile</span></span>
<span data-ttu-id="2ca38-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2ca38-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ca38-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2ca38-113">-Force</span></span>
<span data-ttu-id="2ca38-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="2ca38-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca38-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2ca38-115">-Name</span></span>
<span data-ttu-id="2ca38-116">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ca38-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="2ca38-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ca38-117">-PassThru</span></span>
<span data-ttu-id="2ca38-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="2ca38-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2ca38-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2ca38-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca38-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ca38-120">-ResourceGroupName</span></span>
<span data-ttu-id="2ca38-121">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ca38-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="2ca38-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2ca38-122">-Confirm</span></span>
<span data-ttu-id="2ca38-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2ca38-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca38-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ca38-124">-WhatIf</span></span>
<span data-ttu-id="2ca38-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2ca38-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ca38-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2ca38-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca38-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ca38-127">CommonParameters</span></span>
<span data-ttu-id="2ca38-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ca38-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ca38-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ca38-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ca38-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ca38-130">INPUTS</span></span>

### <span data-ttu-id="2ca38-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2ca38-131">System.String</span></span>

## <span data-ttu-id="2ca38-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ca38-132">OUTPUTS</span></span>

### <span data-ttu-id="2ca38-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2ca38-133">System.Boolean</span></span>

## <span data-ttu-id="2ca38-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ca38-134">NOTES</span></span>

## <span data-ttu-id="2ca38-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ca38-135">RELATED LINKS</span></span>

[<span data-ttu-id="2ca38-136">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="2ca38-136">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="2ca38-137">Új – AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="2ca38-137">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="2ca38-138">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="2ca38-138">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="2ca38-139">Teszt-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="2ca38-139">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


