---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: 165a85f48bc39608bd636073b4b12427e0a81bf0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013015"
---
# <span data-ttu-id="3c21e-101">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="3c21e-101">Get-AzProfile</span></span>

## <span data-ttu-id="3c21e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c21e-102">SYNOPSIS</span></span>
<span data-ttu-id="3c21e-103">A telepített modulok által támogatott szolgáltatásprofilok beszerzése.</span><span class="sxs-lookup"><span data-stu-id="3c21e-103">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="3c21e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c21e-104">SYNTAX</span></span>

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## <span data-ttu-id="3c21e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c21e-105">DESCRIPTION</span></span>
<span data-ttu-id="3c21e-106">A telepített modulok által támogatott szolgáltatásprofilok beszerzése.</span><span class="sxs-lookup"><span data-stu-id="3c21e-106">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="3c21e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3c21e-107">EXAMPLES</span></span>

### <span data-ttu-id="3c21e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3c21e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

<span data-ttu-id="3c21e-109">A szolgáltatás által támogatott szolgáltatásprofil beszerzése</span><span class="sxs-lookup"><span data-stu-id="3c21e-109">Get the service profile supported by the KeyVault module</span></span>

## <span data-ttu-id="3c21e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c21e-110">PARAMETERS</span></span>

### <span data-ttu-id="3c21e-111">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="3c21e-111">-ListAvailable</span></span>
<span data-ttu-id="3c21e-112">A telepített modulok által támogatott szolgáltatásprofilok listázása</span><span class="sxs-lookup"><span data-stu-id="3c21e-112">List all service profiles supported by installed modules</span></span>

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

### <span data-ttu-id="3c21e-113">-ModuleName</span><span class="sxs-lookup"><span data-stu-id="3c21e-113">-ModuleName</span></span>
<span data-ttu-id="3c21e-114">Az ellenőrizendő modul neve</span><span class="sxs-lookup"><span data-stu-id="3c21e-114">The name of the module to check</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c21e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c21e-115">CommonParameters</span></span>
<span data-ttu-id="3c21e-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c21e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c21e-117">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c21e-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c21e-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c21e-118">INPUTS</span></span>

### <span data-ttu-id="3c21e-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="3c21e-119">None</span></span>

## <span data-ttu-id="3c21e-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c21e-120">OUTPUTS</span></span>

### <span data-ttu-id="3c21e-121">Microsoft. Azure. Command. profil. CommonModule. PSAzureServiceProfile</span><span class="sxs-lookup"><span data-stu-id="3c21e-121">Microsoft.Azure.Commands.Profile.CommonModule.PSAzureServiceProfile</span></span>

## <span data-ttu-id="3c21e-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c21e-122">NOTES</span></span>

## <span data-ttu-id="3c21e-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c21e-123">RELATED LINKS</span></span>
