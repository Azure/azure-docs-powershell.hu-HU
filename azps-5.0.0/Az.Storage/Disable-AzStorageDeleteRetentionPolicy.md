---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: c8a32cb86ace86cb0f2775db98f49f57408be6f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186354"
---
# <span data-ttu-id="7c426-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7c426-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="7c426-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c426-102">SYNOPSIS</span></span>
<span data-ttu-id="7c426-103">Tiltsa le a törlés adatmegőrzési házirendet az Azure Storage blob szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="7c426-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="7c426-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c426-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c426-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c426-105">DESCRIPTION</span></span>
<span data-ttu-id="7c426-106">A **disable-AzStorageDeleteRetentionPolicy** parancsmag letiltja a törlés-adatmegőrzési házirendet az Azure Storage blob szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="7c426-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="7c426-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7c426-107">EXAMPLES</span></span>

### <span data-ttu-id="7c426-108">1. példa: a blob-szolgáltatás adatmegőrzési házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="7c426-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="7c426-109">Ez a parancs letiltja a blob-szolgáltatás adatmegőrzési házirendjének törlését.</span><span class="sxs-lookup"><span data-stu-id="7c426-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="7c426-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c426-110">PARAMETERS</span></span>

### <span data-ttu-id="7c426-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="7c426-111">-Context</span></span>
<span data-ttu-id="7c426-112">Azure Storage Context objektum</span><span class="sxs-lookup"><span data-stu-id="7c426-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="7c426-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c426-113">-DefaultProfile</span></span>
<span data-ttu-id="7c426-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c426-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c426-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c426-115">-PassThru</span></span>
<span data-ttu-id="7c426-116">DeleteRetentionPolicyProperties megjelenítése</span><span class="sxs-lookup"><span data-stu-id="7c426-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="7c426-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7c426-117">-Confirm</span></span>
<span data-ttu-id="7c426-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7c426-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c426-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c426-119">-WhatIf</span></span>
<span data-ttu-id="7c426-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7c426-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c426-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7c426-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c426-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c426-122">CommonParameters</span></span>
<span data-ttu-id="7c426-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c426-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c426-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c426-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c426-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c426-125">INPUTS</span></span>

### <span data-ttu-id="7c426-126">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7c426-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7c426-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c426-127">OUTPUTS</span></span>

### <span data-ttu-id="7c426-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7c426-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="7c426-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c426-129">NOTES</span></span>

## <span data-ttu-id="7c426-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c426-130">RELATED LINKS</span></span>