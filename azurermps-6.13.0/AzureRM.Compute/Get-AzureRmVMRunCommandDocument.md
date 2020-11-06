---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
ms.openlocfilehash: 070fe50f74db08caab375a97d4d8ff6be3e970ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495157"
---
# <span data-ttu-id="f210f-101">Get-AzureRmVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="f210f-101">Get-AzureRmVMRunCommandDocument</span></span>

## <span data-ttu-id="f210f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f210f-102">SYNOPSIS</span></span>
<span data-ttu-id="f210f-103">Futtassa a Futtatás parancsot.</span><span class="sxs-lookup"><span data-stu-id="f210f-103">Get run command document.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f210f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f210f-104">SYNTAX</span></span>

```
Get-AzureRmVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f210f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f210f-105">DESCRIPTION</span></span>
<span data-ttu-id="f210f-106">Futtassa a Futtatás parancsot.</span><span class="sxs-lookup"><span data-stu-id="f210f-106">Get run command document.</span></span>

## <span data-ttu-id="f210f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f210f-107">EXAMPLES</span></span>

### <span data-ttu-id="f210f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f210f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="f210f-109">A ' westus ' "RunPowerShellScript" parancsára vonatkozó konkrét futtatási parancsot kap.</span><span class="sxs-lookup"><span data-stu-id="f210f-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>
<span data-ttu-id="f210f-110">Get-AzureRmVMRunCommandDocument-hely $loc</span><span class="sxs-lookup"><span data-stu-id="f210f-110">Get-AzureRmVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="f210f-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="f210f-111">Example 2</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="f210f-112">Az összes elérhető Futtatás parancs az "westus" listában.</span><span class="sxs-lookup"><span data-stu-id="f210f-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="f210f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f210f-113">PARAMETERS</span></span>

### <span data-ttu-id="f210f-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="f210f-114">-CommandId</span></span>
<span data-ttu-id="f210f-115">A parancs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f210f-115">The command id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f210f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f210f-116">-DefaultProfile</span></span>
<span data-ttu-id="f210f-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f210f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f210f-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="f210f-118">-Location</span></span>
<span data-ttu-id="f210f-119">A futtatott parancsok lekérdezésének helye.</span><span class="sxs-lookup"><span data-stu-id="f210f-119">The location upon which run commands is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f210f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f210f-120">CommonParameters</span></span>
<span data-ttu-id="f210f-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f210f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f210f-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f210f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f210f-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f210f-123">INPUTS</span></span>

### <span data-ttu-id="f210f-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f210f-124">System.String</span></span>

## <span data-ttu-id="f210f-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f210f-125">OUTPUTS</span></span>

### <span data-ttu-id="f210f-126">Microsoft. Azure. commands. számítási. Automation. models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="f210f-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="f210f-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f210f-127">NOTES</span></span>

## <span data-ttu-id="f210f-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f210f-128">RELATED LINKS</span></span>
