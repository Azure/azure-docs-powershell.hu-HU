---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 83dbf747e2ddcd001320ac746b7c505df73a8169
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927634"
---
# <span data-ttu-id="e4dc1-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e4dc1-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="e4dc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4dc1-102">SYNOPSIS</span></span>
<span data-ttu-id="e4dc1-103">Frissíti (frissítse a kiszolgálót) az Azure webhely-helyreállítási szolgáltatótól kapott adatokat.</span><span class="sxs-lookup"><span data-stu-id="e4dc1-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="e4dc1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e4dc1-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4dc1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e4dc1-105">DESCRIPTION</span></span>
<span data-ttu-id="e4dc1-106">Az **Update-AzRecoveryServicesAsrServicesProvider** parancsmag frissíti az Azure webhely-helyreállítási szolgáltatótól kapott információkat.</span><span class="sxs-lookup"><span data-stu-id="e4dc1-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="e4dc1-107">Ezzel a parancsmagkal elindíthatja a helyreállítási szolgáltatótól kapott információk frissítését.</span><span class="sxs-lookup"><span data-stu-id="e4dc1-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="e4dc1-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e4dc1-108">EXAMPLES</span></span>

### <span data-ttu-id="e4dc1-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="e4dc1-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="e4dc1-110">Elindítja a megadott ASR-szolgáltatótól származó adatok frissítését, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="e4dc1-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e4dc1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4dc1-111">PARAMETERS</span></span>

### <span data-ttu-id="e4dc1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4dc1-112">-DefaultProfile</span></span>
<span data-ttu-id="e4dc1-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4dc1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e4dc1-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4dc1-114">-InputObject</span></span>
<span data-ttu-id="e4dc1-115">Megadja azt az ASR-szolgáltató-objektumot, amely azonosítja azt a kiszolgálót, amelynek az adatait frissíteni (frissíteni kell.)</span><span class="sxs-lookup"><span data-stu-id="e4dc1-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4dc1-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4dc1-116">-Confirm</span></span>
<span data-ttu-id="e4dc1-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e4dc1-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4dc1-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4dc1-118">-WhatIf</span></span>
<span data-ttu-id="e4dc1-119">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e4dc1-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4dc1-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4dc1-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4dc1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4dc1-121">CommonParameters</span></span>
<span data-ttu-id="e4dc1-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4dc1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4dc1-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4dc1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4dc1-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4dc1-124">INPUTS</span></span>

### <span data-ttu-id="e4dc1-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e4dc1-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="e4dc1-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4dc1-126">OUTPUTS</span></span>

### <span data-ttu-id="e4dc1-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="e4dc1-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e4dc1-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e4dc1-128">NOTES</span></span>

## <span data-ttu-id="e4dc1-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4dc1-129">RELATED LINKS</span></span>

[<span data-ttu-id="e4dc1-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e4dc1-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="e4dc1-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e4dc1-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
