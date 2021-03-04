---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: 25526e7c83746b67a5272ab94f3d523947795c1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929273"
---
# <span data-ttu-id="c5bf3-101">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c5bf3-101">Enable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="c5bf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="c5bf3-103">Engedélyezze a statikus webhelyet az Azure Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="c5bf3-103">Enable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="c5bf3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c5bf3-104">SYNTAX</span></span>

```
Enable-AzStorageStaticWebsite [[-IndexDocument] <String>] [[-ErrorDocument404Path] <String>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5bf3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c5bf3-105">DESCRIPTION</span></span>
<span data-ttu-id="c5bf3-106">Az **Enable-AzStorageStaticWebsite** parancsmag statikus webhelyet engedélyez az Azure Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="c5bf3-106">The **Enable-AzStorageStaticWebsite** cmdlet enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="c5bf3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c5bf3-107">EXAMPLES</span></span>

### <span data-ttu-id="c5bf3-108">1. példa: Statikus webhely engedélyezése az Azure Storage-fiókhoz</span><span class="sxs-lookup"><span data-stu-id="c5bf3-108">Example 1: Enable static website for the Azure Storage account</span></span>
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

<span data-ttu-id="c5bf3-109">Ez a parancs engedélyezi a statikus webhelyet az Azure Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="c5bf3-109">This command enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="c5bf3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5bf3-110">PARAMETERS</span></span>

### <span data-ttu-id="c5bf3-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c5bf3-111">-Context</span></span>
<span data-ttu-id="c5bf3-112">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="c5bf3-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="c5bf3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5bf3-113">-DefaultProfile</span></span>
<span data-ttu-id="c5bf3-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5bf3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5bf3-115">-ErrorDocument404Path</span><span class="sxs-lookup"><span data-stu-id="c5bf3-115">-ErrorDocument404Path</span></span>
<span data-ttu-id="c5bf3-116">A hibadokumentum elérési útja, amely a 404-es hibakód kibocsátáskor jelenik meg (ami azt jelenti, hogy egy böngésző nem létező lapot kér.)</span><span class="sxs-lookup"><span data-stu-id="c5bf3-116">The path to the error document that should be shown when a 404 is issued (meaning, when a browser requests a page that does not exist.)</span></span>

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

### <span data-ttu-id="c5bf3-117">-IndexDocument</span><span class="sxs-lookup"><span data-stu-id="c5bf3-117">-IndexDocument</span></span>
<span data-ttu-id="c5bf3-118">A tárgymutató-dokumentum neve az egyes címtárakban.</span><span class="sxs-lookup"><span data-stu-id="c5bf3-118">The name of the index document in each directory.</span></span>

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

### <span data-ttu-id="c5bf3-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5bf3-119">-PassThru</span></span>
<span data-ttu-id="c5bf3-120">Statikus webhelybeállítás megjelenítése a ServiceProperties szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="c5bf3-120">Display Static Website setting in ServiceProperties.</span></span>

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

### <span data-ttu-id="c5bf3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5bf3-121">-Confirm</span></span>
<span data-ttu-id="c5bf3-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c5bf3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5bf3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5bf3-123">-WhatIf</span></span>
<span data-ttu-id="c5bf3-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c5bf3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5bf3-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5bf3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5bf3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5bf3-126">CommonParameters</span></span>
<span data-ttu-id="c5bf3-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5bf3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5bf3-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5bf3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5bf3-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5bf3-129">INPUTS</span></span>

### <span data-ttu-id="c5bf3-130">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c5bf3-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c5bf3-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5bf3-131">OUTPUTS</span></span>

### <span data-ttu-id="c5bf3-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="c5bf3-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="c5bf3-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c5bf3-133">NOTES</span></span>

## <span data-ttu-id="c5bf3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5bf3-134">RELATED LINKS</span></span>
