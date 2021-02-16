---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: e97e89c1ab7160f1eb06c9c94cd5620a48b0463e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165723"
---
# <span data-ttu-id="0696f-101">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0696f-101">Enable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="0696f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0696f-102">SYNOPSIS</span></span>
<span data-ttu-id="0696f-103">Engedélyezze a statikus webhelyet az Azure Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="0696f-103">Enable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="0696f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0696f-104">SYNTAX</span></span>

```
Enable-AzStorageStaticWebsite [[-IndexDocument] <String>] [[-ErrorDocument404Path] <String>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0696f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0696f-105">DESCRIPTION</span></span>
<span data-ttu-id="0696f-106">Az **Enable-AzStorageStaticWebsite** parancsmag statikus webhelyet engedélyez az Azure Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="0696f-106">The **Enable-AzStorageStaticWebsite** cmdlet enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="0696f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0696f-107">EXAMPLES</span></span>

### <span data-ttu-id="0696f-108">1. példa: Statikus webhely engedélyezése az Azure Storage-fiókhoz</span><span class="sxs-lookup"><span data-stu-id="0696f-108">Example 1: Enable static website for the Azure Storage account</span></span>
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

<span data-ttu-id="0696f-109">Ez a parancs engedélyezi a statikus webhelyet az Azure Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="0696f-109">This command enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="0696f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0696f-110">PARAMETERS</span></span>

### <span data-ttu-id="0696f-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0696f-111">-Context</span></span>
<span data-ttu-id="0696f-112">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="0696f-112">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0696f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0696f-113">-DefaultProfile</span></span>
<span data-ttu-id="0696f-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0696f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0696f-115">-ErrorDocument404Path</span><span class="sxs-lookup"><span data-stu-id="0696f-115">-ErrorDocument404Path</span></span>
<span data-ttu-id="0696f-116">A hibadokumentum elérési útja, amely a 404-es hibakód kibocsátáskor jelenik meg (ami azt jelenti, hogy egy böngésző nem létező lapot kér.)</span><span class="sxs-lookup"><span data-stu-id="0696f-116">The path to the error document that should be shown when a 404 is issued (meaning, when a browser requests a page that does not exist.)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0696f-117">-IndexDocument</span><span class="sxs-lookup"><span data-stu-id="0696f-117">-IndexDocument</span></span>
<span data-ttu-id="0696f-118">A tárgymutató-dokumentum neve az egyes címtárakban.</span><span class="sxs-lookup"><span data-stu-id="0696f-118">The name of the index document in each directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0696f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0696f-119">-PassThru</span></span>
<span data-ttu-id="0696f-120">Statikus webhelybeállítás megjelenítése a ServiceProperties szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="0696f-120">Display Static Website setting in ServiceProperties.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0696f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0696f-121">-Confirm</span></span>
<span data-ttu-id="0696f-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0696f-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0696f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0696f-123">-WhatIf</span></span>
<span data-ttu-id="0696f-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0696f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0696f-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0696f-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0696f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0696f-126">CommonParameters</span></span>
<span data-ttu-id="0696f-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0696f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0696f-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0696f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0696f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0696f-129">INPUTS</span></span>

### <span data-ttu-id="0696f-130">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0696f-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0696f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0696f-131">OUTPUTS</span></span>

### <span data-ttu-id="0696f-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="0696f-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="0696f-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0696f-133">NOTES</span></span>

## <span data-ttu-id="0696f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0696f-134">RELATED LINKS</span></span>
