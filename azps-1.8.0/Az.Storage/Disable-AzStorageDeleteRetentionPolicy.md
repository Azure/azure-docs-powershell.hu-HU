---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: fad4e01b06182d689e105f4b5e6c6a580e1b20b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668700"
---
# <span data-ttu-id="28ff9-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="28ff9-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="28ff9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="28ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="28ff9-103">Tiltsa le a törlés adatmegőrzési házirendet az Azure Storage blob szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="28ff9-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="28ff9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="28ff9-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28ff9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="28ff9-105">DESCRIPTION</span></span>
<span data-ttu-id="28ff9-106">A **disable-AzStorageDeleteRetentionPolicy** parancsmag letiltja a törlés-adatmegőrzési házirendet az Azure Storage blob szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="28ff9-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="28ff9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="28ff9-107">EXAMPLES</span></span>

### <span data-ttu-id="28ff9-108">1. példa: a blob-szolgáltatás adatmegőrzési házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="28ff9-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="28ff9-109">Ez a parancs letiltja a blob-szolgáltatás adatmegőrzési házirendjének törlését.</span><span class="sxs-lookup"><span data-stu-id="28ff9-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="28ff9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="28ff9-110">PARAMETERS</span></span>

### <span data-ttu-id="28ff9-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="28ff9-111">-Context</span></span>
<span data-ttu-id="28ff9-112">Azure Storage Context objektum</span><span class="sxs-lookup"><span data-stu-id="28ff9-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="28ff9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28ff9-113">-DefaultProfile</span></span>
<span data-ttu-id="28ff9-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28ff9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28ff9-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28ff9-115">-PassThru</span></span>
<span data-ttu-id="28ff9-116">DeleteRetentionPolicyProperties megjelenítése</span><span class="sxs-lookup"><span data-stu-id="28ff9-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="28ff9-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="28ff9-117">-Confirm</span></span>
<span data-ttu-id="28ff9-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="28ff9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28ff9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28ff9-119">-WhatIf</span></span>
<span data-ttu-id="28ff9-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="28ff9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28ff9-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="28ff9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28ff9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28ff9-122">CommonParameters</span></span>
<span data-ttu-id="28ff9-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="28ff9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28ff9-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28ff9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28ff9-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="28ff9-125">INPUTS</span></span>

### <span data-ttu-id="28ff9-126">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="28ff9-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="28ff9-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28ff9-127">OUTPUTS</span></span>

### <span data-ttu-id="28ff9-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="28ff9-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="28ff9-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="28ff9-129">NOTES</span></span>

## <span data-ttu-id="28ff9-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28ff9-130">RELATED LINKS</span></span>
