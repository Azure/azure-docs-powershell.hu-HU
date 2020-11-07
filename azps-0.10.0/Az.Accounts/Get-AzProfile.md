---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: d541c943c8dc9779cdf340440078ca2fd2fb36e1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841054"
---
# <span data-ttu-id="2f4d0-101">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="2f4d0-101">Get-AzProfile</span></span>

## <span data-ttu-id="2f4d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f4d0-102">SYNOPSIS</span></span>
<span data-ttu-id="2f4d0-103">A telepített modulok által támogatott szolgáltatásprofilok beszerzése.</span><span class="sxs-lookup"><span data-stu-id="2f4d0-103">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="2f4d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f4d0-104">SYNTAX</span></span>

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## <span data-ttu-id="2f4d0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f4d0-105">DESCRIPTION</span></span>
<span data-ttu-id="2f4d0-106">A telepített modulok által támogatott szolgáltatásprofilok beszerzése.</span><span class="sxs-lookup"><span data-stu-id="2f4d0-106">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="2f4d0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2f4d0-107">EXAMPLES</span></span>

### <span data-ttu-id="2f4d0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2f4d0-108">Example 1</span></span>
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

<span data-ttu-id="2f4d0-109">A szolgáltatás által támogatott szolgáltatásprofil beszerzése</span><span class="sxs-lookup"><span data-stu-id="2f4d0-109">Get the service profile supported by the KeyVault module</span></span>

## <span data-ttu-id="2f4d0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f4d0-110">PARAMETERS</span></span>

### <span data-ttu-id="2f4d0-111">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="2f4d0-111">-ListAvailable</span></span>
<span data-ttu-id="2f4d0-112">A telepített modulok által támogatott szolgáltatásprofilok listázása</span><span class="sxs-lookup"><span data-stu-id="2f4d0-112">List all service profiles supported by installed modules</span></span>

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

### <span data-ttu-id="2f4d0-113">-ModuleName</span><span class="sxs-lookup"><span data-stu-id="2f4d0-113">-ModuleName</span></span>
<span data-ttu-id="2f4d0-114">Az ellenőrizendő modul neve</span><span class="sxs-lookup"><span data-stu-id="2f4d0-114">The name of the module to check</span></span>

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

### <span data-ttu-id="2f4d0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f4d0-115">CommonParameters</span></span>
<span data-ttu-id="2f4d0-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f4d0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f4d0-117">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2f4d0-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f4d0-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f4d0-118">INPUTS</span></span>

### <span data-ttu-id="2f4d0-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="2f4d0-119">None</span></span>

## <span data-ttu-id="2f4d0-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f4d0-120">OUTPUTS</span></span>

### <span data-ttu-id="2f4d0-121">Microsoft. Azure. Command. profil. CommonModule. PSAzureServiceProfile</span><span class="sxs-lookup"><span data-stu-id="2f4d0-121">Microsoft.Azure.Commands.Profile.CommonModule.PSAzureServiceProfile</span></span>

## <span data-ttu-id="2f4d0-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f4d0-122">NOTES</span></span>

## <span data-ttu-id="2f4d0-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f4d0-123">RELATED LINKS</span></span>
