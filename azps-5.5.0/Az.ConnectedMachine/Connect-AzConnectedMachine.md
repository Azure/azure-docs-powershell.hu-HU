---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/connect-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
ms.openlocfilehash: 281d456eb7612914bac546b3d361238bb5056626
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209927"
---
# <span data-ttu-id="6e45e-101">Connect-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="6e45e-101">Connect-AzConnectedMachine</span></span>

## <span data-ttu-id="6e45e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e45e-102">SYNOPSIS</span></span>
<span data-ttu-id="6e45e-103">API-val regisztrálhat egy új gépet, és ezáltal nyomon követhető erőforrást hozhat létre a ARM</span><span class="sxs-lookup"><span data-stu-id="6e45e-103">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="6e45e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6e45e-104">SYNTAX</span></span>

```
Connect-AzConnectedMachine [-ResourceGroupName] <String> [-Location] <String> [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-DefaultProfile] <PSObject>] [[-PSSession] <PSSession[]>] [[-Tag] <Hashtable>]
 [[-Proxy] <Uri>] [<CommonParameters>]
```

## <span data-ttu-id="6e45e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6e45e-105">DESCRIPTION</span></span>
<span data-ttu-id="6e45e-106">API-val regisztrálhat egy új gépet, és ezáltal nyomon követhető erőforrást hozhat létre a ARM</span><span class="sxs-lookup"><span data-stu-id="6e45e-106">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="6e45e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6e45e-107">EXAMPLES</span></span>

### <span data-ttu-id="6e45e-108">1. példa: A csatlakoztatott gépként csatlakoztatott gépbe való berakás</span><span class="sxs-lookup"><span data-stu-id="6e45e-108">Example 1: Onboards the machine you're on as a connected machine</span></span>
```powershell
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name linux_eastus1_1 -Location eastus

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3235e

Name             Location OSName   Status     ProvisioningState
----             -------- ------   ------     -----------------
linux_eastus1_1  eastus   linux    Connected  Succeeded
```

<span data-ttu-id="6e45e-109">Csatlakoztatva van a csatlakoztatott géphez.</span><span class="sxs-lookup"><span data-stu-id="6e45e-109">Onboards the machine you're on as a connected machine.</span></span>

### <span data-ttu-id="6e45e-110">2. példa: Távoli gép begépre történő beraktatása csatlakoztatott eszközként</span><span class="sxs-lookup"><span data-stu-id="6e45e-110">Example 2: Onboards a remote machine as a connected device</span></span>
```powershell
PS C:\> $session = Connect-PSSession -ComputerName WINBOX
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-rg -Name win_eastus1_1 -Location eastus -PSSession $session

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3236a

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
win_eastus1_1  eastus   windows  Connected  Succeeded
```

<span data-ttu-id="6e45e-111">Távoli gépbe való bekapcsolás csatlakoztatott eszközként a PowerShell-remoting használatával.</span><span class="sxs-lookup"><span data-stu-id="6e45e-111">Onboards a remote machine as a connected device using PowerShell remoting.</span></span>
<span data-ttu-id="6e45e-112">Megjegyzés: Jelenleg csak a Windows támogatott célként.</span><span class="sxs-lookup"><span data-stu-id="6e45e-112">Note: only Windows as the target is supported at this time.</span></span>

## <span data-ttu-id="6e45e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e45e-113">PARAMETERS</span></span>

### <span data-ttu-id="6e45e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e45e-114">-DefaultProfile</span></span>
<span data-ttu-id="6e45e-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e45e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e45e-116">-Location</span><span class="sxs-lookup"><span data-stu-id="6e45e-116">-Location</span></span>
<span data-ttu-id="6e45e-117">A létrehozott ConnectedMachine helye.</span><span class="sxs-lookup"><span data-stu-id="6e45e-117">The location for the created ConnectedMachine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e45e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6e45e-118">-Name</span></span>
<span data-ttu-id="6e45e-119">A géphez használt név.</span><span class="sxs-lookup"><span data-stu-id="6e45e-119">The name that will be used for this machine.</span></span>
<span data-ttu-id="6e45e-120">A rendszer alapértelmezés szerint az állomásnevet használja.</span><span class="sxs-lookup"><span data-stu-id="6e45e-120">The hostname is used by default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e45e-121">-Proxy</span><span class="sxs-lookup"><span data-stu-id="6e45e-121">-Proxy</span></span>
<span data-ttu-id="6e45e-122">A proxykiszolgáló által használt URI</span><span class="sxs-lookup"><span data-stu-id="6e45e-122">The URI for the proxy server to use</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e45e-123">-PSSession</span><span class="sxs-lookup"><span data-stu-id="6e45e-123">-PSSession</span></span>
<span data-ttu-id="6e45e-124">Ha meg van adva, akkor a gépeket az Azure-ba befutó parancs minden PSSession-en belül fog futni.</span><span class="sxs-lookup"><span data-stu-id="6e45e-124">When specified, the command that onboards machines to Azure will be run within each PSSession.</span></span>
<span data-ttu-id="6e45e-125">MEGJEGYZÉS: Ez a lehetőség jelenleg csak Windows rendszeren működik.</span><span class="sxs-lookup"><span data-stu-id="6e45e-125">NOTE: This only works on Windows for now.</span></span>

```yaml
Type: System.Management.Automation.Runspaces.PSSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e45e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e45e-126">-ResourceGroupName</span></span>
<span data-ttu-id="6e45e-127">Annak az erőforráscsoportnak a neve, amelybe fel szeretné adni a gépet.</span><span class="sxs-lookup"><span data-stu-id="6e45e-127">The name of the resource group you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e45e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6e45e-128">-SubscriptionId</span></span>
<span data-ttu-id="6e45e-129">Annak az előfizetésnek az azonosítója, amelybe fel szeretné adni a gépet.</span><span class="sxs-lookup"><span data-stu-id="6e45e-129">The ID of the subscription you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e45e-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="6e45e-130">-Tag</span></span>
<span data-ttu-id="6e45e-131">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="6e45e-131">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e45e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e45e-132">CommonParameters</span></span>
<span data-ttu-id="6e45e-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e45e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e45e-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e45e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e45e-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e45e-135">INPUTS</span></span>

## <span data-ttu-id="6e45e-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e45e-136">OUTPUTS</span></span>

## <span data-ttu-id="6e45e-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6e45e-137">NOTES</span></span>

<span data-ttu-id="6e45e-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6e45e-138">ALIASES</span></span>

## <span data-ttu-id="6e45e-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e45e-139">RELATED LINKS</span></span>

